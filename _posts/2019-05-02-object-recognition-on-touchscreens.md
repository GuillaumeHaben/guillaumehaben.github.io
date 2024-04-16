---
layout: post
title:  "Object recognition on touchscreens"
date:   2019-05-02
excerpt: "During our third year at TELECOM Nancy, we had the opportunity to work on a real-life project for 6 months. I was very lucky to be assigned to one of the most innovative projects that were offered to us. Here is what we've done."
image: images/object-recognition-on-touchscreens/logo-1.jpg
tag:
- Innovation
- Touchscreen
- Object
- Recognition
published: true
---
## Introduction
Reaching the final year at TELECOM Nancy was a big step to obtain our engineering degree, but we were still not completely prepared to the professional life. The main topic of this year consisted in the realization of a project offered by a company which we referred as [industrial projects](http://telecomnancy.univ-lorraine.fr/en/entreprise/industrial-projects).<br /> 
This task aimed to make students aware of how to address real-world problems faced by companies. In small teams, we had to design a solution, from the specifications to the delivery phase, after having correctly identified the needs of the company. 

## Context
We were three students to work on the Object Recognition project offered by [Digilor](https://www.digilor.fr/), a French startup created a few years ago. This young society focuses on digital marketing and sells large touch monitors alongside with applications and customer support. 

<figure class="third">
    <a href="/images/object-recognition-on-touchscreens/touchscreens-1.jpg"><img src="/images/object-recognition-on-touchscreens/touchscreens-1.jpg"></a>
    <a href="/images/object-recognition-on-touchscreens/touchscreens-2.jpg"><img src="/images/object-recognition-on-touchscreens/touchscreens-2.jpg"></a>
    <a href="/images/object-recognition-on-touchscreens/touchscreens-3.jpg"><img src="/images/object-recognition-on-touchscreens/touchscreens-3.jpg"></a>
</figure> 

This kind of device are becoming common around us: in fast foods, museums, show rooms... In fact, from a commercial point of view, the user interaction they offer is often a great marketing asset.
If you're familiar with the startup world, you should know that the key of success is to keep being innovative on the market. If you have a good idea, you will quickly be joined by competitors. So if you want to keep being the leader on a market (and you WANT to), you constantly have to find new ideas, new concepts, new products...

Like a lot of other startups, this one was using 120% of it resources to provide outstanding work. The industrial project at TELECOM Nancy was a way to get three young and motivated nearly-engineers at a cheap price. Good for us, it also meant that we were going to do something that really mattered. It was a true need and the startup put its entire trust in us. This was not this kind of boring projects in big companies which would never have been used. We were being asked to find a solution to a problem the company had no idea how to solve it. 

Digilor wanted to offer to the end users a new way of interacting with applications by giving them the ability to use objects on touchscreens. The fact that people could be able to manipulate objects, for example, miniatures of a customer’s products, was really appealing, but the research in this domain was only at its early stages.

## The project
As I said it earlier, this was something completely new for our startup that didn't have a clue on how to answer this problem and Digilor made an important bet by trusting students to find a solution in less than half a year.

### Research & Developement 
In the begining of the project, we spent a lot of time to read research papers and to look for what other companies were selling. Despite being long, we needed that to understand what was already existing and what solution was possible to implement. 

#### Screens

First, we identified three potential touchscreen technologies that we could use: infrared, resistive and capacitive pictured below.
<figure>
    <a href="/images/object-recognition-on-touchscreens/hardware-technologies.png"><img src="/images/object-recognition-on-touchscreens/hardware-technologies.png"></a>
</figure>

* Infrared touchscreens 

IR recognition works with a grid of laser beams fixed on top of regular screens. Touches are triggered by the interception of the beams. It can work with any pointers and it is a cheap technology that can easily be set on various touchscreens. It has some drawbacks, like it's difficulty to work in lightly environments, the lack of multitouch...

* Resistive touchscreens

This technology was common a few years ago. It detects touches when a pressure occurs on the screen, creating a contact between two layers as shown in the picture. This kind of touchscreen were the one we could find in GPS devices, Nintendo DS... This technology is less suitable for big screens and the quality is not so good.

* Capacitive touchscreens

This new technology becomes more and more widespread. Nowadays, almost all smartphones embed it. It works thanks to an electrically charged screen. A touch is detected when a potential difference is happening on the screen. It is important to understand that it works due to the ground given by the human body. It means that a touch pen only works because you are holding it and your body transfer its ground to it. The rubber part is made with some conductive materials and is only there to simulate the finger's texture. This was a crucial information we had to know. We decided to realize our project by using this type of screen because they had the best user experience and are becoming cheaper and cheaper.

#### Objects

The road to find a suitable solution was long. We quickly decided to use passive objects. Active objects embed electronics inside them to simulate a ground, but we didn't want to have objects dependent on batteries, potentially making noises and being definitely more expensive. Our first tests were funny. As you can see below, we tried magnetic chips linked by conductive ink, twisted copper wire and even a big metallic slice with bolts in it. This last object was not perfect and couldn't be used for a commercial solution, but enabled us to perform our first software tests. 

<figure>
    <a href="/images/object-recognition-on-touchscreens/objects.png"><img src="/images/object-recognition-on-touchscreens/objects.png"></a>
</figure>

**It is at this point that we discovered a very important property of capacitive touchscreens**. 

One of the main challenge we had to address was to have objects that were still detected by the screen when untouched (remember that it needs a ground to work). In a nutshell, our discovery led us to understand that objects could use the own screen's ground. This is one of the reasons why our objects have three points of contact (One point using the others as ground). The other reason is because we used the geometric properties of triangles to create and identify unique objects. The application was fun to develop. We created a library using Python and [Kivy](https://kivy.org/) to detect objects' position and orientation. We developed a Back-End app to identify objects and a prototype, showcasing a potential usage of this idea. It consisted in an application that could change the background color of the screen by rotating an object used as a color picker. 

<figure class="third">
    <a href="/images/object-recognition-on-touchscreens/logo-1.jpg"><img src="/images/object-recognition-on-touchscreens/logo-1.jpg"></a>
    <a href="/images/object-recognition-on-touchscreens/prototype-1.png"><img src="/images/object-recognition-on-touchscreens/prototype-1.png"></a>
    <a href="/images/object-recognition-on-touchscreens/prototype-2.png"><img src="/images/object-recognition-on-touchscreens/prototype-2.png"></a>
</figure>

Reaching the end of our project, we finally found the perfect way to build our objects. We created a numerical model and 3D-printed it by using a particular PLA conductive filament. It worked perfectly and was definitively more gorgeous than our first prototypes!

### Project management
The main complexity of this project resided in the fact that it was a research project. We only had six months to get familiar with the problem, to draw a state of the art, to learn technologies and to come up with a solution that could be sold (without forgetting that we still had classes to attend). I think that one of the main reason for its success was due to how well we managed this project. Among our team, we all had our experience with the Student Association, so we all knew the basics of how to correctly lead projects. By that, I simply mean properly defining goals, fixing deadlines for tasks and distributing the work between us.

In a fairly natural way, we set up 15-minutes long meetings every week to follow up on our work where we simply talked about what we did the week before and what we'll aim to do for the next one.

Here is the main planning we followed, the one top being the provisional one, and the one below the effective one. It is interesting to notice that the research part was definitely longer than what we were expecting, but we were able to overcome this issue by starting the development phase earlier by using our prototypes.

<figure>
    <a href="/images/object-recognition-on-touchscreens/planning.png"><img src="/images/object-recognition-on-touchscreens/planning.png"></a>
</figure>

## Final thoughts

This project was by far the most interesting project I had at school. Having the responsibility of finding a complete solution to a real-world problem was so exciting. We ended up by inventing something totally new. Our solution turned out to be cheap (One object being < 5€) and delightful. It is during our project that Microsoft unveiled the [Microsoft Dial](https://www.microsoft.com/en-us/p/surface-dial/925r551sktgn?activetab=pivot%3aoverviewtab), but compared to our solution, it was expensive, heavy and needed to be charged. Our objects were customizable (you could easily print anything you'd like) and this was the whole point. Before attending our final oral defense at school, Digilor had already found two companies willing to buy the solution. And it was only the beginning... 

Here is the official video!

<iframe width="640" height="360" src="https://www.youtube-nocookie.com/embed/QD7KIPxZl0M?controls=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>
<br />

## Edit: 2024

I had the opportunity to visit a friend who is working at CERN in Geneva. There, we went to the visitor center and I really enjoyed the exhibition and small museum. I was as surprised as pleased to see that our invention was being used for an Air Hockey table!


<figure>
    <a href="/images/object-recognition-on-touchscreens/edit.jpeg"><img src="/images/object-recognition-on-touchscreens/edit.jpeg"></a>
</figure>

I learned that this was the product of another company. 8 years later we can still be proud of our job, especially because they didn't implemented object identification and orientation!