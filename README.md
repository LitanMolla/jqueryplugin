# jQuery Plugin List

## Counter Plugin

### *Dorkari Files/CDN/Codes*

- [Live Demo] (https://bfintal.github.io/Counter-Up/demo/demo.html)
- js cdn
- (https://cdnjs.cloudflare.com/ajax/libs/waypoints/2.0.3/waypoints.min.js)
- (https://cdnjs.cloudflare.com/ajax/libs/Counter-Up/1.0.0/jquery.counterup.min.js)

### *Custom js file e add kora lagbe*

``` bash
jQuery(document).ready(function($) {
            $('.counter').counterUp({
                delay: 10,
                time: 1000
            });
        });
```

### *Html e add kora lagbe/jekhane counter output dekhte chai*

```
class="counter"
```


## CountDown Plugin

- [Live Demo] (https://codepen.io/AllThingsSmitty/pen/JJavZN)

- ### *Custom js file e add kora lagbe*

```
(function () {
  const second = 1000,
        minute = second * 60,
        hour = minute * 60,
        day = hour * 24;

  //I'm adding this section so I don't have to keep updating this pen every year :-)
  //remove this if you don't need it
  let today = new Date(),
      dd = String(today.getDate()).padStart(2, "0"),
      mm = String(today.getMonth() + 1).padStart(2, "0"),
      yyyy = today.getFullYear(),
      nextYear = yyyy + 1,
      dayMonth = "09/30/",
      birthday = dayMonth + yyyy;
  
  today = mm + "/" + dd + "/" + yyyy;
  if (today > birthday) {
    birthday = dayMonth + nextYear;
  }
  //end
  
  const countDown = new Date(birthday).getTime(),
      x = setInterval(function() {    

        const now = new Date().getTime(),
              distance = countDown - now;

        document.getElementById("days").innerText = Math.floor(distance / (day)),
          document.getElementById("hours").innerText = Math.floor((distance % (day)) / (hour)),
          document.getElementById("minutes").innerText = Math.floor((distance % (hour)) / (minute)),
          document.getElementById("seconds").innerText = Math.floor((distance % (minute)) / second);

        //do something later when date is reached
        if (distance < 0) {
          document.getElementById("headline").innerText = "It's my birthday!";
          document.getElementById("countdown").style.display = "none";
          document.getElementById("content").style.display = "block";
          clearInterval(x);
        }
        //seconds
      }, 0)
  }());
  ```

  - ### *Html e add kora lagbe/jekhane countdown output chai*

  ```
  id="days"
  id="hours"
  id="minutes"
  id="seconds"
  ```    

  ## LightBox

  - [Live Demo] (https://lokeshdhakar.com/projects/lightbox2/)
  - [GitHub URL] (https://github.com/lokesh/lightbox2)  
  
### *আপনার কাজটি সঠিকভাবে সম্পন্ন করার জন্য নিচের ধাপগুলো অনুসরণ করুন:*

- GitHub থেকে ফাইল ডাউনলোড করুন:

GitHub রিপোজিটরি থেকে Code বাটনে ক্লিক করুন।
Download ZIP অপশন সিলেক্ট করে ZIP ফাইলটি ডাউনলোড করুন।

-  ফাইল আনজিপ করুন:

ডাউনলোড করা ZIP ফাইলটি আনজিপ করুন। আনজিপ করার পর আপনার ফোল্ডারের ভিতরে থাকা ফাইলগুলো দেখতে পাবেন। 

-  ফাইল কপি করুন:

আনজিপ করা ফোল্ডারের মধ্যে dist নামের একটি ফোল্ডার থাকবে।
সেখান থেকে lightbox.min.css এবং lightbox.min.js ফাইল দুটি কপি করুন।
এরপর images নামের ফোল্ডার থেকে সব ছবি কপি করুন।

-  ফাইল পেস্ট করুন:

কপি করা CSS, JS ফাইল এবং images ফোল্ডারের সব ছবি আপনার প্রজেক্ট ফোল্ডারে পেস্ট করুন।

-  HTML ফাইলে CSS এবং JS লিঙ্ক করুন:

- and follow this template

```
<a href="images/image-2.jpg" data-lightbox="roadtrip">Image #2</a>
```

## VenoBox


- [Download URL] (https://veno.es/venobox/)  

- ### ১. ফাইল ডাউনলোড করুন:
প্রথমে নিচের লিংকে ক্লিক করে সমস্ত ফাইল ডাউনলোড করুন।  

URL: (https://veno.es/venobox/)

- ### ২. ফাইল আনজিপ করুন:
ডাউনলোডকৃত .zip ফাইলটি আপনার পিসিতে আনজিপ করুন।

- ### ৩. dist ফোল্ডার খুলুন:
আনজিপ করার পরে ফোল্ডারের ভেতরে dist নামের একটি ফোল্ডার পাবেন।

- ### ৪. ফাইল কপি করুন:
dist ফোল্ডারের ভেতর থেকে নিচের দুটি ফাইল কপি করুন:
venobox.min.js
venobox.min.css

- ### ৫. আপনার প্রজেক্ট ফোল্ডারে পেস্ট করুন:
উপরের ফাইল দুটি আপনার প্রজেক্ট ফোল্ডারের মধ্যে পেস্ট করুন।

- ### ৬. HTML ফাইলে লিঙ্ক করুন:
আপনার প্রজেক্টের HTML ফাইলে CSS এবং JS ফাইলগুলো লিঙ্ক করুন

- ### js for image

```
new VenoBox({
    selector: '.my-image-links',
    numeration: true,
    infinigall: true,
    share: true,
    spinner: 'rotating-plane'
});
```

- ### Image Html

```
<a class="my-image-links" data-gall="gallery01" href="image01-big.jpg"><img src="image01-small.jpg"></a>
```


- ### js for video

```
new VenoBox({
    selector: '.my-video-links',
});
```

- ### html for video 

```
<a class="my-video-links" data-autoplay="true" data-vbtype="video" href="http://youtu.be/xxx">Youtube</a>
```
