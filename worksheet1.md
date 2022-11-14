---
title: "UFCFGL-30-1 Programming in C++"
author: []
date: "2020-18-10"
keywords: [Example]
...

# Setting up :: Worksheet(1)

```c++
#include <cstdlib>
int main(){
    std::system("git --help");
    return 0;
};
```

The marking scheme for this session is as follows:

- Task 1 : 0 marks
- Task 2 : 0 marks

> No Marks are awarded for this worksheet, however, all tasks MUST be completed before preceding.
>
> All work is handed in via git/GitLab and will require the skills demonstrated in this worksheet.



## Working with existing Projects

As we will use existing repositories for most of the tasks in this module, we will explore the process of forking a project in more detail.

A fork is a copy of a project that allows you to make changes without actually changing the original project. This makes it a good way of taking a project as a starting point to then go off and do your own thing.



We will explore this process by forking the example project found at the following url:

https://gitlab.uwe.ac.uk/ng-renney/example



You will need to be logged in to see the ```fork``` option. You should see a page something like this:

![gitlab page](../../guides/git/git_resources/gitlab1.png)



The fork button is found in the top right of the pages main body:

![top right of the pages main body](../../guides/git/git_resources/gitlab2.png)



**When GitLab asks what namespace you wish to add the repo to, select your user account.**



Once you have forked the project you should notice that you now have a repo that no longer uses

https://gitlab.uwe.ac.uk/ng-renney/example.git but instead takes the form (where your-username represents your personal gitlab username):

https://gitlab.uwe.ac.uk/your-username/example.git

Read these urls carefully, and ensure that you are using the correct one going forward.



With a version of the repo forked for your own use, you can clone the repo and edit it locally.

This is described in the **'Git Submissions'** resource [[here]](https://gitlab.uwe.ac.uk/ng-renney/cpp_resources_2020/-/blob/master/git/git-submissions.md) which you should have read and can also be looked up in the 'Git Reference' resource sheet [[here]](https://gitlab.uwe.ac.uk/ng-renney/cpp_resources_2020/-/blob/master/git/git-reference.md). If you haven't, go through those sheets (as well as the [git intro](https://gitlab.uwe.ac.uk/ng-renney/cpp_resources_2020/-/blob/master/git/intro-to-git.md)) and you should be ready to tackle your first set of tasks.



# Tasks



**Task 1 **

- Create a git repo locally and add a readme.md file

- Add some content to the readme.md
- Create a repo on Gitlab and push the contents to the repo



**Task 2 ** 

- Fork the repo at https://gitlab.uwe.ac.uk/ng-renney/example.git 
- Clone your newly forked example project

- Add some text to the example.txt file
- Push your changes so they are visible in you Gitlab project.

