# Firebase analytics In Flutter

## Plugin Needs
[firebase_core: ^1.2.0](https://pub.dev/packages/firebase_core)
[firebase_analytics: ^8.1.0](https://pub.dev/packages/firebase_analytics)

## main.dart
```bash
    void main() async {
  		WidgetsFlutterBinding.ensureInitialized();
	 	await Firebase.initializeApp();  // Put here
	 	runApp(MyApp());
	}
```

## Create new Class analytics_service.dart
```bash
import 'package:firebase_analytics/firebase_analytics.dart';
import 'package:firebase_analytics/observer.dart';
import 'package:flutter/material.dart';

class AnalyticsService {
  final FirebaseAnalytics _analytics = FirebaseAnalytics();
  FirebaseAnalyticsObserver getAnalyticsObserver() => FirebaseAnalyticsObserver(analytics: _analytics);

  Future setUserProperties({@required String userId}) async {
    await _analytics.setUserId(userId);
  }

  Future logLogin({@required String loginMethod}) async {
    await _analytics.logLogin(loginMethod: loginMethod);
  }

  Future logEvent(String eventName, {dynamic data}) async {
    //for firebase
    try {
      await _analytics.logEvent(
        name: eventName,
        parameters: data,
      );
      print("Firebase Event");
    } on Exception catch (e) {
      // TODO
      print("Firebase Event Error : ${e.toString()}");
    }
  }
}
```
## Usage
```bash
AnalyticsService analyticsService = AnalyticsService();
var eventData = {'token': token};
await analyticsService.logEvent(firebaseEvents.offerViewed, data: eventData);
```