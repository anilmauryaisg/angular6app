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

Replace with :  

```HTML
<app-header></app-header>
<router-outlet></router-outlet>
<app-footer></app-footer>
```

3.) add bootstrap cdn in src/index.html file just before /head.

```HTML
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
```


4.) open /src/app/header/header.component.html

Replace with following script
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
      <a class="navbar-brand" routerLink="/">Indydesk CRM</a>
    </div>
    <div id="navbar" class="collapse navbar-collapse">
      <ul class="nav navbar-nav">
        <li routerLinkActive="active"><a  routerLink="/home">Home</a></li>
        <li routerLinkActive="active"><a  routerLink="/about-us">About</a></li>
        <li routerLinkActive="active"><a  routerLink="/contact-us">Contact</a></li>
      </ul>
    </div><!--/.nav-collapse -->
  </div>
</nav>
```

5.) open /src/app/footer/footer.component.html

Replace with following script

```HTML
<div class="container-fluid padding-0">
  <footer>
    <div class="container">
    <div class="row">
      <div class="col-sm-4">
        <ul>
          <li><a href="javascript:void(0);">Home</a></li>
          <li><a href="javascript:void(0);">About Us</a></li>
          <li><a href="javascript:void(0);">Contact Us</a></li>
          <li><a href="javascript:void(0);">Privacy Policy</a></li>
        </ul>
      </div>

      <div class="col-sm-4">
        <ul>
          <li><a href="javascript:void(0);">Home</a></li>
          <li><a href="javascript:void(0);">About Us</a></li>
          <li><a href="javascript:void(0);">Contact Us</a></li>
          <li><a href="javascript:void(0);">Privacy Policy</a></li>
        </ul>
      </div>

      <div class="col-sm-4">
        <ul>
          <li><a href="javascript:void(0);">Home</a></li>
          <li><a href="javascript:void(0);">About Us</a></li>
          <li><a href="javascript:void(0);">Contact Us</a></li>
          <li><a href="javascript:void(0);">Privacy Policy</a></li>
        </ul>
      </div>
    </div>
    </div>
      
  </footer>
  <div class="col-sm-12 copyright">
    <p class="text-center">copyright&copy; indydesk.com</p>
  </div>

</div>
```

6.) open /src/app/home/home.component.html

Replace with following script

```HTML
<div class="container-fluid" style="background: #f7f6f6;">

  <div class="starter-template">
    <div class="col-sm-12">
      <h1>Manage your business, easily</h1>
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. </p>
      <button class="btn btn-lg btn-primary">Get Started</button>
  </div>
  </div>
</div>
<div class="container">
  <div class="fav-product">
     <div class="row">
          <h1 class="text-center" style="margin: 30px 0; text-decoration: underline;">Popular Products</h1>
          <div class="col-md-4">
            <h2>Heading</h2>
            <p>Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus. Etiam porta sem malesuada magna mollis euismod. Donec sed odio dui. </p>
            <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
          </div>
          <div class="col-md-4">
            <h2>Heading</h2>
            <p>Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus. Etiam porta sem malesuada magna mollis euismod. Donec sed odio dui. </p>
            <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
         </div>
          <div class="col-md-4">
            <h2>Heading</h2>
            <p>Donec sed odio dui. Cras justo odio, dapibus ac facilisis in, egestas eget quam. Vestibulum id ligula porta felis euismod semper. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.</p>
            <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
          </div>
    </div>

     <div class="row">
          <div class="col-md-4">
            <h2>Heading</h2>
            <p>Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus. Etiam porta sem malesuada magna mollis euismod. Donec sed odio dui. </p>
            <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
          </div>
          <div class="col-md-4">
            <h2>Heading</h2>
            <p>Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus. Etiam porta sem malesuada magna mollis euismod. Donec sed odio dui. </p>
            <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
         </div>
          <div class="col-md-4">
            <h2>Heading</h2>
            <p>Donec sed odio dui. Cras justo odio, dapibus ac facilisis in, egestas eget quam. Vestibulum id ligula porta felis euismod semper. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.</p>
            <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
          </div>
    </div>
</div>
</div>
```

6.) open /src/app/app-routing.module.ts

Replace with following script

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