##Dropdown open close alpine js
```angular2html
<div x-data={open:false}>
                <a href="javascript:void(0);" x-on:click.prevent="open=!open"
                   class="relative flex items-center text-black hover:text-white group hover:bg-primary font-normal px-5 py-3 text-sm transition duration-150 ease-in-out capitalize">
                   button
                </a>
                <div x-show="open" class="absolute left-0 md:left-full lg:left-64 top-32 md:top-8 m-3 z-50"
                     x-transition:enter="transition transform origin-top-left ease-out duration-200"
                     x-transition:enter-start="opacity-0 scale-75"
                     x-transition:enter-end="opacity-100 scale-100"
                     x-transition:leave="transition transform origin-top-left ease-out duration-200"
                     x-transition:leave-start="opacity-100 scale-100"
                     x-transition:leave-end="opacity-0 scale-75"
                >
                    <div>
                        dropdown code
                    </div>
                </div>
            </div>
```