#Angular6 Basic Tutorial

Setup:

Step.1) Download Nodejs latest version from following site.

https://nodejs.org/en/download/

Step.2) Install Nodejs.

click on windows start button and type nodejs, click on Node.js Command Prompt

You can check version : node -v, npm -v

Step.3) Then install the Angular CLI globally.

npm install -g @angular/cli

Step.4) Create a new project

ng new angular6App --style=scss --routing


Step 5: Test the application

cd angular6App

ng serve --open

http://localhost:4200/

<h1>Customize Application</h1>


1.) Generate New Component : 

ng generate component header

ng generate component footer

ng generate component home     

ng generate component about-us

ng generate component contact

and hit enter after every command

2.) open src/app/app.component.html file

Replace every thing with :  

```HTML
<app-header></app-header>
<router-outlet></router-outlet>
<app-footer></app-footer>
```

3.) add bootstrap cnd in src/index.html file just before /head .

```HTML
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
```


4.) open /src/app/header/header.component.html
Replace with following
```HTML
<nav class="navbar navbar-inverse navbar-fixed-top">
  <div class="container">
    <div class="navbar-header">
      <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
      <a class="navbar-brand" href="#">Project name</a>
    </div>
    <div id="navbar" class="collapse navbar-collapse">
      <ul class="nav navbar-nav">
        <li class="active"><a href="#">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div><!--/.nav-collapse -->
  </div>
</nav>
```

5.) open /src/app/footer/footer.component.html

```HTML
<div class="container-fluid">
	<footer>
		<p class="text-center">copyright&copy; indydesk.com</p>
	</footer>
</div>
```

6.) open /src/app/home/home.component.html

```HTML
<div class="container-fluid">

  <div class="starter-template">
  	<div class="col-sm-12">
	    <h1>Manage your business, easily with Indydesk</h1>
	    <p>Try our Secure, Simple, Easy business tool to Manage Your Project, Tasks, Employees.</p>
	</div>
  </div>

</div>
```
6.) open /src/app/home/home.component.scss
```HTML
.starter-template {
    margin: 51px auto;    
    text-align: center;
    padding: 100px 0;
    width: 800px;
}

.starter-template h1 {
	font-size: 50px;

}
```

7.) open /src/app/app-routing.module.ts

```HTML
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';
import { HomeComponent } from './home/home.component';
import { AboutUsComponent } from './about-us/about-us.component';
import { ContactUsComponent } from './contact-us/contact-us.component';
const routes: Routes = [
	{
		path: '',
		component: HomeComponent
	},
	{
		path: 'home',
		component: HomeComponent
	},
	{
		path: 'about-us',
		component: AboutUsComponent
	},
	{
		path: 'contact-us',
		component: ContactUsComponent
	},

];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```