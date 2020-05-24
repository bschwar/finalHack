README
The web application we created is a method of teaching students, at the pace they need with the methods they need. The basics of the system are that a student takes a pretest and then if they pass, they are considered to know the subject. If else the website selects a method of teaching by placing three numbers into a random number generator, which determines how the student will be taught: with flashcards, with a video, or with an article. This is based on the result of the random number generator as if the value is <= the flashcard value, they are taught by flashcards, else if the value is <= the flashcard value + the video value, they are taught by an article, else they are taught by a video. If the student passes the post-test, the application will increase the likelihood that the student is taught the same way in the future. If they fail the post-test, the likelihood of them being taught by the other 2 methods that were not chosen will increase, and they are sent back to the tutor page. 

In addition to the success of the student affecting themselves, whenever a student successfully completes they also increase the likelihood of the “global student” being taught with the same tactic. Whenever a new student is created, the values from the global student (which starts at 200,200,200) are divided by ten, and then are used as their values of the random number generator. Since the “global student” represents the trend of all past students, it can allow newer students to be taught in a “recommended” while the better tactic for them is being found.

If students leave the current page or the website, their data is saved and they can return to where they left off, no matter the amount of progress they made on the page. This data is stored in a database with the tables. This includes users that contain the users’ id, username, password, and values for the random number generator. Pages that store the name of each class, their category, the iframe data for the tutoring methods, and the HTML for the tests. Finally scores which has the userid, pageid, and the score of the user on the given page. To save space on the scores table, whenever a user logs out their data on the table for untouched pages is removed, and then returned when they log back in.


The app itself has a vast database of classes and tests for the student to use. These are categorized by type and subtype, but they can also be searched for at the top of the site. Yet there is no way for a website to have everything a student might want to study. This is where the teacher accounts come in.

Teacher accounts act exactly like student accounts in all ways but one; when being created the user adds a teacher id to the sign-up form. Having a teacher-id allows the user to create a new class with its own tests and tutor materials. The teacher can then send out their teacher code and if students enter a classroom using the code they can take the new class created by the teacher.

In order to protect the users of the website, despite the lack of truly personal information, the website contains various protection measures. This includes hashing the password before it is stored in the SQL database and using bind.param when interacting with the database.

In conclusion, The problem we as high schoolers face is that the learning instructions were always one style, whether it is text or video. The problem is that everyone learns differently. With Digital Aristotle, using Machine Learning through a random number generator that improves upon itself when either yourself or someone else learns something, it can teach students the way that they need to be taught. The internet contains a wealth of knowledge with so many possible methods of teaching students. The web application not only learns how to teach the student best as individuals, but also allows the student to experience many different ways of learning.

Aristotle himself said, “Knowing yourself is the beginning of all wisdom”. Our web app follows this principle because the website knowing the student, and the student knowing how they learn best is the foundation of a strong education.

									Script

Good afternoon judges of Planet hacks! Over the past 24 hours, my team and I have been working vigorously to create a new platform for online learning. With the current pandemic, both teachers and students have been faced with the challenge to adapt to a variety of Non-traditional virtual learning experiences. And it is precisely through these experiences that we, as high school students, have had the opportunity to learn which instructional lessons were effective and others that weren’t. So just like how Aristotle tutored Alexander the Great, Digital Aristotle, was created with the underlying purpose to help students learn at their own pace with personalized and adaptive learning techniques. 

So to make this idyllic dream a reality, we first began on the sign-up page of the web-application where we implemented a teacher ID feature. Accounts that create a Teacher ID have access to 2 unique features. First off, teachers have the ability to create a class with specific instructional plans adapted for their students to complete.  And secondly, once these tests have been created then completed by the students, the teacher gets personalized feedback about how individual students best learned the content so that they can utilize the data for future instructional planning.

When logging in, the website compares the password typed into the login box with the hashed password stored in the SQL database. As displayed in the video, if the passwords do not match, the user is shown an error. Transitioning to the student interface, you are first brought to the home page where you have the ability to learn from a variety of topics such as math, science, social studies, languages, and coding; each of which includes individual sub-categories. In this demo, we take you through the algebra course where we begin with a pre-test. If you score 4 or higher, then you get a screen that states you are proficient in the sub-topic. However, if this is a skill you are unfamiliar with, the program utilizes Machine Learning to adapt to your individual studying techniques using a random number generator. This random number generator is used to increase the likeliness of the website auto-selecting your most efficient teaching technique so that you are able to learn new topics more effectively. The taskbar can also be employed to easily navigate through many of the topics offered by digital Aristotle. Lastly, as a student, you have the ability to sign up for a teacher’s Class using their individualized code with the ability to do their assigned problem sets and review additional flashcards, videos, and articles associated with the topic.

Just like Aristotle once said, “Education is an ornament to prosperity.” and it is this fountain of knowledge that we hope to share with the world through Digital Aristotle. Lastly, If you have any questions, feel free to ask us in discord and again, thank you so much for your time and we hope you enjoyed it!
