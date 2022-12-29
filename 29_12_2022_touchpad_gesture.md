# linux_app 

#### ল্যাপটপের অন্যতম প্রধান ইনপুট ডিভাইস হলো টাচপ্যাড (touchpad)। এর একটি অন্যতম বৈশিষ্ট্য হলো gesture সাপোর্ট। যারা MacBook ব্যবহার করেন তারা জানেন কতটা smooth হতে পারে এই gesture। কয়েক বছর ধরে উইন্ডোজ তাদের precision ড্রাইভারের মাধ্যমে মোটামুটি ভালো মানের gesture সাপোর্ট দিয়ে যাচ্ছে। 
লিনাক্স বেশ পিছিয়ে ছিল এই gesture সাপোর্টের দিক থেকে। তবে Wayland ও libinput ডেভেলপ করার অবস্থা কিছুটা উন্নতি হয়েছে। এখন Gnome 40 এ বেশ কিছু ১:১ gesture আছে। এছাড়া অনেক gnome ও gtk অ্যাপ pinch to zoom, rotate, back/forward এসব সাপোর্ট করে Wayland এ। এছাড়া সম্প্রতি elementary OS Odin এ ডেভলপাররা gesture সাপোর্ট নিয়ে বেশ কিছু কাজ করেছেন।
আমি gnome ব্যবহার করি, তাই এখানে gnome ও gtk অ্যাপ নিয়ে কথা হবে বেশি।
Gnome 40 তে বেশ কিছু gesture সাপোর্ট করলেও  নিম্মোক্ত extension দিয়ে অপশন আরো বাড়াতে পারেন। এটা Wayland ও x11 দুটোতেই কাজ করে। https://extensions.gnome.org/.../4245/gesture-improvements/
তবে আপনি যদি শুধু Xorg ব্যবহার করেন তাহলে নিচের টুলগুলো ব্যবহার করে আরো ভালো gesture সাপোর্ট পেতে পারেন। যদি আপনার touchpad এ এই gesture গুলোর সাপোর্ট থাকে।
Touchegg
---------------
এটা হচ্ছে মূল টুল। এটা ব্যাকগ্রাউন্ডে কাজ করবে। এটা পাবেন এখানে https://github.com/JoseExposito/touchegg
ওই পেজে ইনস্টল প্রক্রিয়া দেওয়া আছে।
এই টুলের gui হিসেবে ব্যবহার করতে পারেন Touche অ্যাপটি। 
https://github.com/JoseExposito/touche
ওই লিংকে ইনস্টল করার পদ্ধতি দেওয়া আছে। এছাড়া flatpak ভার্সন ও ব্যবহার করতে পারেন flathub থেকে।
Touchegg কে কনফিগার করার জন্য এই gui টুল। Gnome ব্যবহারকারীরা এর সাথে x11 gesture extension ব্যবহার করতে পারেন। https://extensions.gnome.org/extension/4033/x11-gestures/
আশা করি, ল্যাপটপ ব্যবহারকারী যারা আছেন, তাদের উপকার হবে।

## Gui in flatfunk
https://flathub.org/apps/details/com.github.joseexposito.touche
