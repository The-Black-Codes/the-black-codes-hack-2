# Church Directory 

## Challenge 
For this challenge we will be dealing with building complex objects and manipulating them. This may involve reading and writing to a file and creating a user interface for entering data. Since the challenge is not about designing good UI your interface may be console based or a simple HTML page, 
but it will need to have all the functionality required for the level of challenge you choose.

## Creating a Test Case
We’ll continue to use test driven development. No matter the level you choose write a test case before you start coding. Then write enough code to pass the test. 
Once you have a passing test write more tests and refactor you code to accommodate all possible tests.

## Level 1
The first step in an active church directory is to be able to enter the information for each family in the church. Store this information to a file for future retrieval.

The secretary needs to be able to input an address with city and state along with a home phone number (if one exists) for each family. The family may only be a single person or a mother and father with children and everything in between. Each person will have a name (first, middle, last), 
a date of birth, and some will have a cell phone number.

A sample JSON object may be:

```json
family: {
  address: "123 Main St",
  city: "Somewhere",
  state: "TN",
  adults: [
    {
      name: "Calvin Foster",
      birthDate: 1988-03-31,
      cellPhone: "6155551234"
    },
    {
      name: "Nicole Ahima-Foster",
      birthDate: 1988-01-16,
      cellPhone: "6155551235"
    }
  ]
  children: [
    {
      name: "Sophia Foster",
      birthDate: 2016-05-21,
      cellPhone: null
    }
  ]
}
```

A Step Further
Make your directory indexable. The church has asked that they be able to look up families by last name so they can quickly update their information such as change of address or new child.

Level 2
Now that you have built them a directory the youth minister wants to automate sending out flier about an upcoming event to all of the families with children between the ages of 10 and 12. He normally handwrites these invitations but asked if you could personalize them automatically.

The text of the flier should read:


[LastName] Family
[Street Address]
[City] [State]
We are having a lock in for children ages 10 - 12 at the church on September 26, 2017. The youth staff wanted to make sure that [children’s first name between ages 10 - 12] know they are invited and need to bring a sleeping bag, tooth brush/paste, pajamas, and their favorite board game.

Doors will shut at 7:30 pm and open back up at 7:30 am.

Thanks,
Curtis Crutchfield
Church Youth Minister

A Step Further
Since your flier for the youth minister was so successful the college/singles minister has asked you to send out an invitation to a singles retreat to all adults in their 20’s that are in a single adult family. If they have children she wants it to ask them to leave the kids at home.

The invitation should read:


[Full Name]
[Street Address]
[City] [State]
You are invited to a singles retreat for young professionals at church. It will be October 15 - 17, 2017 at [Choose a location].

Please bring a sleeping bag, tooth brush/paste, pajamas, and your favorite board game. All other necessities will be provided by the church.

If they have children include the following as well:


This is an adults only event so please make arrangements for [Children’s First Names] during the retreat.

## Level 3
The church secretary now wants to import the old church directory into the new one so that all the existing families do not have to be reentered. Build a process for importing the JSON file with all of the families in the old directory.

Then go through the new directory and compare it with the information in the old to make sure that families are not duplicated with new ones that have been created. If they are remove the duplicates and/or update the record to show the most current information for each family.

## A Step Further
They church has other directories that are not in JSON but in XML, CSV, etc. To be completely thorough build a process for each type they may have and import the data into the JSON file.
