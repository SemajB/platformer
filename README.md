# Platformer

## An intro to video game programming featuring Halle in a configurable platformer

### Setup

## installing bouncing box with `os install`
NOTE: If you receive an error that says, `os install command not found` the opspark CLI is not installed. To install it, enter the command `npm intall -g opspark` in your bash terminal. 

* Make sure your github and cloud9 accounts are linked to Greenlight
* Open your first website workspace
* go to your bash terminal (located at the bottom of the cloud9 workspace) and type in the command **os install**. Hit enter.
* If prompted, login with your github credentials
* Use your arrow keys to highlight your course and hit enter. hit enter again to confirm.
* Use your arrow keys to highlight bouncing-box and hit enter. hit enter again to confirm.
* open up the index.html file and press Run at the top of your workspace. You will be editing this file.

## Installation with Forking

1. Fork this repository on GitHub by clicking the **Fork** button at the top right of this repository webpage.
2. Clone the project into a Cloud9 workspace.
3. From the `bash` terminal in the console view, cut and paste the following command:
    
        git remote add upstream git@github.com:OperationSpark/platformer.git
    
    This will allow you to pull changes added to the origin / master - the original Operation Spark Platformer repository.
4. Open the `index.html` file and press the green **Run** button at the top of your Cloud9 workspace. This will start a web server hosting your game, and a new pane will open up on the console view at the bottom of your Cloud9 workspace. Click on the link that appears in the console view, then select open. This will open a new brower tab running your game.

### Functions

Functions are encapsulated blocks of code that are designed to perform a set of tasks and can return a value. 

Functions accept data, perform operations on that data, and then produce some result. A **function definition** determines what data the function accepts, what operations are performed, and what result is produced. Here is an example of a function definition called `create`:

```javascript
function create(x, y, scaleX, scaleY, immovable) {
    var platform = game.platforms.create(x, y, 'platform');
    platform.scale.setTo(scaleX || 1, scaleY || 1);
    platform.body.immovable = immovable || true;
    return platform;
}
```

This function accepts 5 pieces of data: `(x, y, scaleX, scaleY, immovable)`, called **parameters**, and uses that data to create a platform which is returned by the function. 

Function definitions simply define how a function operates - it does not execute the code until a **function call** is made. A function call can be made by providing same headline as the function definition but with actual data values, or **arguments**, in the place of the parameters. Here is an example of a function call to the `create` function:

```javascript
platform.create(400, 200, 1, 2, true);
```

This function call will create a platform with an (x,y) location of `(400, 200)` with an X-Scale-Factor of `1`, ad Y-Scale-Factor of `2`, and the immovable property set to `true`. 

*NOTE: The name of function is `create` but it is defined in the `platform` object. When we call this function from anywhere other than inside the `platform` object we must use its full name path of `platform.create`.

### Objective

The idea is to design one level of a platformer game using the functions defined in the `js/factory` folder. You will call these functions in the corresponding files located in the `js/init` folder to create the platforms, add cannons, and collectables that Halle must collect.

It's up to you to design a level that is challenging but doable. Consider <a href="http://phaser.io/examples/v2/category/tweens" target="_blank">tweening</a> platforms, cannons, and collectables.

### Requirements
1. You must create at least 3 cannons in different locations. 
2. You must have at least 3 collectables of different types.
3. You must include at least 4 platforms 
4. Your game must be playable!

### Where to Code?

Open up 3 files:

1. `js/init/platform.js`: Follow the instructions outlined in the file to design all required platforms for the game level.
2. `js/init/cannon.js`: Follow the instructions outlined in the file to design all required cannons for the game level.
3. `js/init/collectable.js`: Follow the instructions outlined in the file to design all required collectables for the game level.

You see instructions on **where to write your code** - keep your code in between the areas **ALL YOUR CODE GOES BELOW HERE** and **ALL YOUR CODE GOES ABOVE HERE**. This will help you make less errors. For example:

```
        ////////////////////////////////////////////////////////////////////////
        // ALL YOUR CODE GOES BELOW HERE ///////////////////////////////////////
        
        collectable.create(type.steve, 200, 170, 6, 0.7);
        
        // ALL YOUR CODE GOES ABOVE HERE ///////////////////////////////////////
        ////////////////////////////////////////////////////////////////////////
```

Code a little, **save your work** (Command / Ctrl + s), switch back to the tab running your game and **refresh the page** (Command / Ctrl + r) to see your work!

Have fun!

###

Pushing your work back to GitHub

After you've designed your level, run (cut and paste) the three following commands:

1. Add all your changes to a changeset:
    
        git add -A
    
2. Commit your changeset:
    
        git commit -m"create awesome platformer game"
    
3. Push your changeset to your GitHub forked repository:
    
        git push
    

Great work! Pat yourselve on the back and show off your game!

Remember that when you comeback to Cloud9, the webserver might have stopped, so to restart it, you must open the `index.html` file and press the green **Run** button. (See step 4 in the Setup section, above).
