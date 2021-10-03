---
layout: post
title: Splittami
---

<a href="https://ggggino.github.io/splittami">Try me</a>

<div class="message">
  Who has to give to whom?
</div>

That's the question that everyone said when a dinner or lunch ends or a friend trip is over.

And I said that every time too, so I decided to search an app that allow me to split the amount quickly.

After some research I found some nice app, but some need registration, some needs download from the store, some needs that a manger fill the configuration of every user.

So at the end I concluded that it would be nice to start build my own version.

### First analisys

The main qualities that the app should have, were **fast usage** and **parallel job**

> **Fast usage** because I want that the users will land directly on the page of the calculation/admin.

> **Parallel job** because I don't want that only one user will fill the data of every single person in the room.

To resolve the first problem I thought that to be fast to use/find, this app shouldn't be downloadble from any kind of store and it shouldn't have any type of registration/login neither.

Since there was no login, I had to find a way to allow users to set their own configurations and send them to other users for calculation.

I was thinking about the various ways of being able to pass data from one device to another and then I opted to generate a qrcode with the object created hashed in md5.
