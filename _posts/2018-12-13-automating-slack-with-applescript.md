---
layout: post
title: Automating Slack with AppleScript
categories: [writings]
---

I recently published an [AppleScript library](https://github.com/samknight/slack_applescript) to help automate common tasks I do in Slack.

For those familiar with AppleScript, the instructions on the library should suffice but for those keen to get started with AppleScript for the first time I’ve created a quick guide for how to launch these Slack automations.

In this tutorial we’ll learn how to set your status to lunch via Spotlight.

**Installation of the Library**

Follow the instructions [on my GitHub repository](https://github.com/samknight/slack_applescript)

**Testing scripts with Script Editor**
 
Open up `Applications -> Utilities ->  Script Editor`

Here you will have a blank sheet. This will act as scratch pad for you to try some scripts. Look at some of the suggestions [on my GitHub repository](https://github.com/samknight/slack_applescript) for inspiration.

Once you've written your script, press the play button to test it.
![Script editor example code](/assets/script_editor.png)

**Executing scripts**

Now that we can run some code, we need a more easily accessible way of running the script. This is where Automator comes in. Automator is a program that helps to chain together various actions on your computer including AppleScripts.

1. Open up `Applications -> Utilities -> Automator`
2. Create a new Application
3. Search for `Run AppleScript` on the actions bar and drag into workflow area on the right.
4. Replace `(* Your script goes here *)` with the script you made in Script Editor 
5. Save the file as the application name of your choice e.g. `Slack Lunch Status` 

![A new Automator application interface](/assets/blank_automator_app.png)
![An Automator app running AppleScript](/assets/applescript_automator_app.png)

Go to the folder where you saved the application and double click. The first time should fail as it won’t have permission to access keyboard functions.

Go to `System Preferences -> Security & Privacy -> Privacy -> Accessibility` and check the box next to the app you saved. You may need to unlock the padlock to do this.

Click the application again and it will now run.

**Trigger via Spotlight**

Whilst clicking an app in Finder is better than running scripts in the script editor there is an even better way to trigger these scripts. 

Launch Spotlight with `cmd + space` and start to type the name of your app. Once it appears press `enter` and it will now run.

![Finding your app via spotlight](/assets/spotlight_search.png)

Voila - you’re on your way to automating your uses with Slack

**Alfred**

If you like triggering things with spotlight then you’ll love [Alfred - Productivity App for macOS](https://www.alfredapp.com). With the power pack add on you can create your own AppleScript workflows directly in Alfred triggered by a keyword. This is a much quicker and more maintainable method than creating Automator applications each time. 

I am by no means an expert on Automator so there may be much more effective ways of creating the above. If you know of a simpler way without tools such as Alfred (see also Keyboard Maestro) then please let me know and I will update this post.

**Extra Credit**

You don’t have to stop at one action per Automator application. You can chain events to create some complex workflows. Just look at the library on the left for hundreds of actions you can add. You can even add custom scripts in javascript and more. See an example below.

![Automator app with 2 actions](/assets/bonus_automator_app.png)


That’s all!
