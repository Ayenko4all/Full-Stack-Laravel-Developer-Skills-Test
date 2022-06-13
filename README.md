
## 1) Voting 

Each voter can vote in zero or more referenda. Each referendum has one or more questions, and each question is a yes/no vote. Write the simplest normalized schema to describe this in generic SQL statements or as an entity-relationship diagram. Point out where the indexes would be if you want to quickly know the results of a given referendum question, but you never expect to query a single voter's voting record. In what way does the nature of the application affect your design judgment about privacy, and what effect would that have on normalization considerations?
- Below is the Model code:
  
Class Referendum

public function questions(){
  return $this->hasMany(Question::class, 'ref_id');
}


Class Question

public function referendum(){
    return $this->belongsTo(Referendum::class, 'ref_id');
}

public function votes(){
    return $this->belongsToMany(Voter::class, 'voter_questions', 'question_id', 'voter_id');
}

Class Voter

public function questions(){
    return $this->belongsTo(Voter::class, 'ref_id');
}

Check the attached link for ER diagram. https://drawsql.app/ayenko-host-link/diagrams/voting-diagram


## 2) Rewriting history with git

-  checkout to your working branch
   
   change the commit message of last commit
   
-  git commit --amend -m "Modified message"

- B will be the same hash as B because we didn't change the message of B


## 3) Service Container
Consider the following Laravel controller:

- Laravel uses what is call service container to resolve all laravel controller. Any dependencies from an injected class through constructor will have been resolved before any other code runs in that controller.

## 4) 
We can simply return has many relationship in the Post Model to get all the comments of a post like the below example: 

public function comments(){
    return $this->hasMany(Comment::class);
}

## 5. Unix tools

find /usr/local -type f -iname "*aardvark*" -print

## 6. CSS

important means that only the !important property value is to be applied to an element and all other declarations on the element are to be ignored.

example {
	font-size: 14px !important;	
}

container #example {
	font-size: 10px;
}

From the above code the first one will override the second declaration
- Front-end developers suggest using it with caution because using !important, it may override the css will do not want it to  be applied to.


## 7 JavaScript

Advantages:

- less characters to type
-  the code is easier to read
-  won't have to debug any missing "}" in your code
-  strict use of indentation

Disadvantages:

-  The lack of braces for function can be problem for some developer
-  requires knowledge of Javascript before using it.
-  can't run a debugger on it directly

 

 
