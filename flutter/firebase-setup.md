# Flutter Firebase setup, use below link for reffer example 

https://github.com/Nitingadhiya/firebase_app


# dependencies:
 ```bash
 firebase_core: ^1.2.0 (https://pub.dev/packages/firebase_core)
 firebase_database: ^6.1.2 (https://pub.dev/packages/firebase_database)
 ```

# main.dart
```bash
import 'package:flutter/material.dart';
import 'custom_data.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(home: CustomData());
  }
}
```

# custom_data.dart
```bash
`initalize firebase on init method`
Helper().firebaseInitalize();

`Create Table`
 _createTableRef = Helper().createTable(widget.app, tableName);

`Add Data in Table`
 Helper().addData(ref, tableName, 'title', params);

`Update Data`
 Helper().updateData(_createTableRef, _tempSnapShot, params);

 `Delete Data`
 Helper().deletePress(_createTableRef, snapshot),
```


# utility / Helper.dart
```bash
 dynamic firebaseInitalize() {
    final referenceDatase = FirebaseDatabase.instance;
    return referenceDatase.reference();
  }

  createTable(widget, tableName) {
    final FirebaseDatabase database = FirebaseDatabase(app: widget);
    return database.reference().child(tableName);
  }

  updateData(_createTableRef, _tempSnapShot, params) {
    _createTableRef.child(_tempSnapShot.key).update(params);
  }

  addData(ref, tableName, keyName, params) {
    ref.child(tableName).push().child(keyName).set(params).asStream();
  }

  deletePress(_createTableRef, snapshot) {
    _createTableRef.child(snapshot.key).remove();
  }
```

Note:- Please use stable version for flutter 
