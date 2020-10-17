---
layout: post
title:      "My first attempt at ASP.NET Core"
date:       2020-10-17 16:57:25 +0000
permalink:  my_first_attempt_at_asp_net_core
---

Having recently completed the Flatiron software engineering bootcamp, I decided to waste no time and begin the job searcing process. In my experience, timing is everything when it comes to job searching, and I did not want to miss the opportunity to find a job that suits me. In addition, this allows me to identify the skills that companies are looking for and fill in any knowledge gaps that may have been missed by the bootcamp. 

One such knowledge gap is the framework used for the backend: Ruby on Rails is not nearly as popular as something like ASP.NET, which is a MVC web framework for Microsoft's .NET Framework and can be written in any language that is supported on the framework, like C# and VB.NET. I thought this would be a perfect opportunity for me to reinforce my programming knowledge since I had already programmed in C# and VB.NET prior to starting at Flatiron, and Flatiron's bootcamp had made me confident in understanding the MVC design pattern.

Oh was I in for a shocker. 

I booted up Visual Studio and created a new project template. The IDE provides many project templates to scaffold your projects from. Some of these terms definitely sound familiar! Let's start with something basic like "Web Application (Model-View-Controller):

![](https://i.imgur.com/KHtGQJc.png)

This is what the scaffolded website looks like when you first run. It is quite bare-bones but definitely provides a little bit more information than the "Yay! You're on Rails!" picture that appears on a Rails project.

![](https://i.imgur.com/Yv9vPOJ.png)

The main HTML page is rendered from a layout so that the nav links at the top exist on every page. Looking at the Layout.html file, I can see the anchor tags that provide links to the "Home" and "Privacy" pages. Also, the place where the main content of the page will render is substituted with a placeholder "@RenderBody()":

![](https://i.imgur.com/9JhAlcn.png)

The @ character, as I have learned, is what is called Razor syntax. This is ASP.NET's way of allowing you to write C# code inside of HTML, which looks exactly like embedded Ruby or JSX syntax!

https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-3.1

The layout's anchor tags appear to act as a router. It is directing the href to a controller named "Home" and actions named "Index" and "Privacy". Looking around the solution explorer, I find a file named HomeController.cs, which looks vaguely similar to the static controller used in Rails. 

![](https://i.imgur.com/m5RQJLp.png)

Notice that both the "Index" and "Privacy" actions have a return statement "return View();". How does the program differentiate between the "Index" and "Privacy" views? Well, it appears that just as in Ruby, it all comes down to a strict convention of naming your files! In the solutions explorer, I open the Views folder, then the Home folder, which contains the views associated with the HomeController. I see two views called "Index.cshtml" and "Privacy.cshtml", which are mapped to the Home controller actions Index and Privacy, respectively:

![](https://i.imgur.com/0RDw7CA.png)



