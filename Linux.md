# Linus Torvalds

## Programming with “good taste”
> What do you think is the most important skill every programmer should posses?

> It’s a thing I call "taste".

> I tend to judge the people I work with not by how proficient they are: some people can churn out a lot of code, but more by how they react to other peoples code, and then obviously by what their own code looks like, and what approaches they chose. That tells me whether they have "good taste" or not, and the thing is, a person without "good taste" often is not very good at judging other peoples code, but his own code often ends up not being wonderfully good.

> But hey, it’s not the only thing. One thing that is very useful, especially in an open source project, is simply the ability to communicate well what you want to do, and how you are going to do it. The ability to explain to others why you do something a certain way is very important, and not everybody has that ability.

> That said, in the end there are also the people who just churn out good code. They may not be good at explaining it, and they may not even have great taste, but the code works well. Sometimes you need another person (one that does have that hard-to-define "taste") to maybe massage the code into a form where it’s useful in the bigger picture, but just the ability to write clear code for difficult problems is obviously a fairly fundamental part of any programmer.

Bad Taste 
```
remove_list_entry(entry)
{
  prev = NULL;
  walk = head; 
  
  // Walk the list 
  
  while (walk != entry) {
    prev = walk;
    walk = walk->next; 
  }
  
  // Remove the entry by updating the head or the previous entry 
  if (!prev)
    head = entry -> next; 
  else 
    prev->next = entry->next; 
}
```

Good Taste
```
remove_list_entry(entry)
{
  // The "indirect" pointer points to the *address* of the thing we'll update
  
  indirect = &head; 
  
  // Walk the list, looking for the thing that points to the entry we want to remove
  
  while((*indirect) !=entry)
    indirect = &(*indirect)->next; 
    
  // .. and just remove it
  *indirect = entry->next; 
}
```

Incorporate edge cases to normal case; think in another way 
