# Codepath-Final-Project
An animal shelter app
http://g.recordit.co/DhoOJbMH7q.gif

http://g.recordit.co/V7BHcR2wny.gif UPDATED PROGRESS GIF
J&S Animal Services Codepath Project - README Template
===
[](https://animaladoptionsite)
# J&S Animal Services 

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
It is an app that will list animals available for adoption within the animal shelter.
 

### App Evaluation
[Evaluation of your app across the following attributes]
- **Category:Lifestyle **
- **Mobile: Mobile First User Experience*
- **Story: Allows users to ind a pet from photos and makes it easy to adopt a pet.**
- **Market: Our market is for anyone that loves pets and is ready to expand their family to a fur-ever pet**
- **Habit: This app isn't very habit forming it allows for potential owners to see available pets and post pets they are no longer able to take care of. **
- **Scope: Users can view photos of pets ready for adoption, users can apply to pets for their choosing.**

## Product Spec

### 1. User Stories (Required and Optional)
Completed User stories/ awaiting TA help
X created signup/login screen
X created launch screen
X TableCell screen

**Required Must-have Stories**

* Signup/Login to create account 
* Stay signed in between use of app
* Show Available pets in shelter 
* Pick a pet to see more information about the pet
* Apply for pet screen 
* Display pet was successfully applied for

**Optional Nice-to-have Stories**

* Apply pet to be listed 
* Favorite Pets to apply later 
* Filter Adoptable Pets 
* Pet Selector Quiz 

### 2. Screen Archetypes

* Signup/Login Page
   * Signup page/login to look at pets
   * Stay signed in between use of app
   * 
* List Of Pets Page
   * Show available pets for adoption 
   * Pet displayed with name, breed and age 
   * Pick a pet to see more information 
   * *BONUS STORY* Filter Adoptable Pets
   * *BONUS STORY* Favorite pets 
* Pet Details Page 
    * Shows more information about the pet 
    * Description of pet 
* Apply For Pet Page 
    * Apply for pet 
    * Display pet was successfully applied for 
* *BONUS STORY* Post a Pet Page  
    * Apply for pet to be posted 
    
* *BONUS STORY* Pet Selector Quiz 
    * Pet selector Quiz 

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Adoptable Pets Page
* Pet Adoption Page
* *BONUS STORY* Pet Selector Quiz 
* *BONUS STORY* Post a Pet Page

**Flow Navigation** (Screen to Screen)

*Login Page 
    *Adoptable Pets
* Adoptable Pets  
   * Pet Details Page 
* Pet Details Page
* Apply For Pets
   * [list screen navigation here]
 


## Wireframes
[Add picture of your hand sketched wireframes in this section]![](https://i.imgur.com/AwnBUmv.jpg)


### [BONUS] Digital Wireframes & Mockups
http://g.recordit.co/DhoOJbMH7q.gif

### [BONUS] Interactive Prototype

## Schema 

### Models
[

|Property  | Type | Description |
|ObjectId  |String|Uniquie Id for user to create account
|Image     |File  | Image uploaded by website|
|Caption   |String| Caption posted by website|
|LikesCount|Number|Number of likes on a post|
|CreatedAt |DateTime|Time when the post was created|
|UpdatedAt |UpdatedTime

]


### Networking

List of network requests by screen
    Login Screen
        (Read/GET) Query where all pet posts are grabbed
        `let query = PFQuery(className:"Uploads")
         query.whereKey("website", equalTo: currentUser)
         query.order(byDescending: "createdAt")
         query.findObjectsInBackground { (posts: [PFObject]?, error: Error?) in
         if let error = error { 
           print(error.localizedDescription)
         } else if let posts = uploads {
              print("Successfully retrieved \(uploads.count) uploads.")
   }
}`
        (Create/POST) Adds pet to favorites
        (Delete) Remove a pet from favorites 
        
   *** BONUS *** Post a Pet
       (Create/POST) Post a Pet for rehome
   
   Pet Details Page
       (Read/GET) Query where pet information is displayed
   
   
