---
layout: post
title: Develop bundle for Symfony ^4.0
---

Every time I have to create a shared Symfony bundle, I forgot how to structure the folders and files.

So here I put some usefull tips/link to speed up the development.

## Structure

The first thing to do is creating a workable Symfony folder, using the instruction described in the download page of symfony.
In this way I can test my bundle in a fresh real installation.

### Create the space for your bundle

Next thing to do is create a folder in the root called "bundles" in order to have a folder that is "outside" the core files.
Create the bundle inside called for example "[GGGGinoRecentyBundle](https://github.com/GGGGino/RecentyBundle)"

<pre>
root
+---bundles
|   \---GGGGino
|       \---RecentyBudle
|           +---composer.json
|           +---.git
|           \---...
+---bin
+---config
</pre>

### Configure symfony to load your bundle

Prepare the autoloader to get your bundle

composer.json
<pre>
{
    ...,
    "autoload": {
        "psr-4": {
            "App\\": "src/",
            "GGGGino\\RecentyBundle\\": "bundles/GGGGino/RecentyBundle/src"
        }
    },
    ...
}
</pre>

To apply this editing to t

Load your bundle inside the symfony project.

> Of course before load the bundle, create it.

bundles.php
{% highlight php %}
<?php

return [
    // other bundles here
    GGGGino\RecentyBundle\GGGGinoRecentyBundle::class => ['all' => true],
];
{% endhighlight %}

## Bundle

Now you can use this [skeleton](https://github.com/treehouselabs/skeleton-bundle), that is a very good starting place.

There are also some good tools to test, beautify you code.

* [Travis-ci](https://travis-ci.org/)
* [Scrutinizer-ci](https://scrutinizer-ci.com/)
* [PHP-CS](https://github.com/FriendsOfPHP/PHP-CS-Fixer)


> Here some of good structured Bundle to take inspiration from

* [GGGGino/SkuskuCartBundle](https://github.com/GGGGino/SkuskuCartBundle)
* [8p/EightPointsGuzzleBundle](https://github.com/8p/EightPointsGuzzleBundle)


