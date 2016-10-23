# Lottery
Kata to turning a class with too many responsibilities into something closer to OOP

### The Lottery entity
The lottery entity it's a stripped down version of the real entity we work with. For the test, you only have to care
about these fields: ``frequency`` and ``draw_time``.

The public interface of the entity is composed mainly by two methods, one (``getLastDrawDate``) for getting the exact 
date and time of the most recent past draw, and another (``getNextDrawDate``) one for getting the next one.

As you can see, there's a big code smell in "duplicated" methods, that are almost exactly the same but change a few 
details. Making the smell go away is your main job.

#### draw_time
This field stores the hour when the draw is taking place. It's a string in format ``hh:mm:ss`` and it represents the
UTC time.

#### frequency
This field tells us which days are the draws taking place. As you can guess by the name, it doesn't represent an actual
date, but a frequency, and it can have the following formats:

* __y1225__: The draw takes place every year on december 25th
* __m24__: The draw takes place on 24th of each month
* __w0100100__: The draw takes place on tuesdays and fridays
* __w0000001__: The draw takes place on sundays
* __d__: The draw takes place every day.

## Executing the tests
As latest PHPUnit version is used by default, at the moment you must have PHP 5.6 or later installed.
Execute composer install, use your favourite IDE and run the tests.
If everything is green, you're ready to go.

## Objective
Take the Lottery entity to the next level: refactor to reduce duplicity of code, change any variable 
naming that doesn't suit for you, introduce design patterns, improve testing, etc.

