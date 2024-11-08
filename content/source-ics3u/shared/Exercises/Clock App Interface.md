---
draft: false
draftSectionTwo: true
enableToc: true
excludeBacklinks: true
created: 2024-11-08T07:00:00.000-0400
createdForSectionTwo: 2024-09-25T00:00:00.000-0400
tags:
---

## Objective 

The objective of this lesson and the related exercises is to reproduce the following interfaces from the iOS Clock app:

![[World Clock.png|350]]

![[Alarms.png|350]]

![[Stopwatch.png|350]]


## Create a new project

In Xcode, from the menus, choose **File > New > Project...** then select the **iOS** tab and then **App**, and finally press the **Next** button:

![[Screenshot 2024-11-08 at 6.50.08 AM.png]]

Name the project **Clock** and then choose the following options for the new project – your organization identifier will be different, and that's OK:

![[Screenshot 2024-11-08 at 6.52.29 AM.png]]

Be sure that **Source Control** is enabled and save your work in an appropriate location on your computer – such as your **Grade 11 Computer Science** folder:

![[Screenshot 2024-11-08 at 6.53.32 AM.png]]

Shortly after the project opens, you will see something like this:

![[Screenshot 2024-11-08 at 6.54.41 AM.png]]

## Set up source control

Change to the Source Control navigator by pressing **Command-2**:

Then create a remote:

![[Screenshot 2024-11-08 at 6.55.11 AM.png]]

You can leave the default options:

![[Screenshot 2024-11-08 at 6.56.22 AM.png]]

## Project organization

Two-finger tap or right-click on the **Clock** folder and choose **Convert to Group**:

![[Screenshot 2024-11-08 at 6.58.02 AM.png]]

Drag and drop the **ClockApp** file, so it is between the **Clock** folder and the **PreviewContent** folder:

![[Screenshot 2024-11-08 at 6.59.01 AM.png]]

Two-finger tap or right-click on the **Clock** folder and make a new group:

![[Screenshot 2024-11-08 at 7.01.06 AM.png]]

Name the new group **Views**:

![[Screenshot 2024-11-08 at 7.01.44 AM.png]]

Drag and drop the **ClockApp** file again, so it is between the **Clock** folder and the **Views** folder:

![[Screenshot 2024-11-08 at 7.02.32 AM.png]]

Select the **ContentView** file:

![[Screenshot 2024-11-08 at 7.03.19 AM.png]]

Place your cursor on line 10, where the structure name is defined:

![[Screenshot 2024-11-08 at 7.04.24 AM.png]]

Two-finger tap at that location, choose **Refactor** and then **Rename...**:

![[Screenshot 2024-11-08 at 7.04.34 AM.png]]

You will see something like this:

![[Screenshot 2024-11-08 at 7.05.23 AM.png]]

Change the name of the structure from **ContentView** to **LandingView**:

![[Screenshot 2024-11-08 at 7.05.57 AM.png]]

Press the **Return** key to save these changes.

Finally, drag and drop the **LandingView** file into the **Views** group:

![[Screenshot 2024-11-08 at 7.06.53 AM.png]]

After completing this organization, now is a good time to commit your work. Use the **Option-Command-C** keyboard shortcut and you will see the interface that shows you recent changes:

![[Screenshot 2024-11-08 at 7.09.48 AM.png]]

Type a commit message of:

> Finished project organization.

... then press the **Stage All** button to indicate that you want to commit all the changes:

![[Screenshot 2024-11-08 at 7.10.35 AM.png]]

Finally, press the small down arrow beside the **Commit** button and choose **Commit and Push**:

![[Screenshot 2024-11-08 at 7.11.15 AM.png]]

## Make the tab view

Return to the Project navigator by pressing **Command-1**, then select the **LandingView** file:

![[Screenshot 2024-11-08 at 7.20.13 AM.png]]

The landing view file is going to, very shortly, contain the tab view portion of the interface:

![[World Clock copy.png|350]]

A tab view works by letting the user switch between multiple other views.

We need to create those views now.

Follow these same steps to create three files:

1. **WorldClockView**
2. **AlarmsView**
3. **StopwatchView**

Here are the steps to create **WorldClockView**.

Two-finger tap on the **Views** group and select **New file from template...**

![[Screenshot 2024-11-08 at 7.21.26 AM.png]]

Then choose **SwiftUI View** and select **Next**:

![[Screenshot 2024-11-08 at 7.22.23 AM.png]]

Name the file **WorldClockView** then press **Create**:

![[Screenshot 2024-11-08 at 7.22.48 AM.png]]

Again, follow these same steps to create the next two views – **AlarmsView** and **StopwatchView**.

When you are finished, your project will look like this:

![[Screenshot 2024-11-08 at 7.24.03 AM.png]]

Switch to **WorldClockView**:

![[Screenshot 2024-11-08 at 7.24.34 AM.png]]

Change the `Text` structure so that it says **World Clock**:

![[Screenshot 2024-11-08 at 7.25.21 AM.png]]

Do the same thing with **AlarmsView**:

![[Screenshot 2024-11-08 at 7.25.44 AM.png]]

And the same with **StopwatchView**:

![[Screenshot 2024-11-08 at 7.26.27 AM.png]]

This allows us to tell each of these views apart when we set up the tab view.

Now return to **LandingView**:

![[Screenshot 2024-11-08 at 7.27.15 AM.png]]

Replace the `VStack` with this code:

```swift
        TabView(selection: Binding.constant(1)) {
            
            WorldClockView()
                .tabItem {
                    Image(systemName: "globe")
                    Text("World Clock")
                }
                .tag(1)
            
            AlarmsView()
                .tabItem {
                    Image(systemName: "alarm.fill")
                    Text("Alarm")
                }
                .tag(2)

            StopwatchView()
                .tabItem {
                    Image(systemName: "stopwatch.fill")
                    Text("Stopwatch")
                }
                .tag(3)

        }
```

Your view will look like this:

![[Screenshot 2024-11-08 at 7.35.14 AM.png]]

In the preview at right, you can now click between the tabs at the bottom of the interface.

Look for this line of code:

```swift
        TabView(selection: Binding.constant(1)) {
```

Try changing the value, `1`, to `2` or `3`. What happens? Why do you think that occurs?

This is a good time to commit and push your work. Use the usual steps and commit and push with this message:

> Got the tab view set up.

## Set dark mode and tint

The **Clock** app is a rare app that always presents a dark interface.

Return to **LandingView** and add the following view modifier on line 34, attached to the `TabView` structure:

![[Screenshot 2024-11-08 at 7.39.06 AM.png]]

Now the interface appears in dark mode at all times.

When a tab is highlighted, the default color of that highlight is blue. There are several ways to adjust this. We can do this now by adding the following line of code, on line 35:

![[Screenshot 2024-11-08 at 7.41.11 AM.png]]

Commit and push your work with this message: 

> Set the color scheme and tint.

## World Clock

### Adjust preview

Switch the **WorldClockView** file:

![[Screenshot 2024-11-08 at 7.42.44 AM.png]]

Notice that we no longer see the tab view or dark mode.

This is because the preview is directly showing us the `WorldClockView` structure:

```swift
#Preview {
    WorldClockView()
}
```

Instead, we should have this preview show us the **LandingView** structure.

Change the code on line 17 to do just that:

![[Screenshot 2024-11-08 at 7.44.17 AM.png]]

Now we can begin working on **WorldClockView** and see the tabs and correct color scheme.

> [!TIP]
> 
> If you don't see the **WorldClockView**, go back to **LandingView**, and make sure that on line 12, the value for the selection on the tab view is set to `Binding.constant(1)`.

### Set the title

Next we will add a title to the interface.

To show a title, we must enable navigation. Navigation is a larger topic we will explore further late on. Right now, we can add the following code to **WorldClockView**:

![[Screenshot 2024-11-08 at 7.53.03 AM.png]]

Nothing changes until we add the `navigationTitle` view modifier:

![[Screenshot 2024-11-08 at 7.53.34 AM.png]]

This is a good time to commit and push your work. Use the usual steps, and the commit message:

> Added a title to the World Clock view.

### Add the toolbar items

The elements at the top of an iOS app interface, highlighted here, are part of what is called the *toolbar*:

![[World Clock 1.png]]

Add the following code below the `navigationTitle` view modifier:

```swift
.toolbar {
	
	ToolbarItem(placement: .topBarLeading) {
		
		Button("Edit") {
			// Does nothing right now
		}
		
	}
	
}
```

Try changing the argument for the `placement` parameter. What happens?

We can add a second button to the toolbar by adding another `ToolbarItem` structure, like this:

![[Screenshot 2024-11-08 at 7.59.41 AM.png]]

We've made great progress, so commit and push with this message:

> Added toolbar items to the interface.

## Exercises

### 1. Finish World Clock

Wrap the `Text` view in a `VStack`:

![[Screenshot 2024-11-08 at 8.02.28 AM.png]]

Now use your knowledge of horizontal and vertical stacks, and SwiftUI Views Mastery as a reference, to complete the user interface for the World Clock:

![[World Clock.png|350]]

### 2. Alarms

Reproduce the Alarms interface:

![[Alarms.png|350]]

### 3. Stopwatch

As an extension, see if you can reproduce the Stopwatch interface:

![[Stopwatch.png|350]]
