# UDBreadCrumb
Component to add breadcrumb links to your dashboard pages

## Please note you need both modules for this to work, just like for the Step Progress Bar

## You need the Breadcrumb module and BreadcrumItem module both installed for this to work

#Demo 
```
    New-UDBreadcrumb -id "BreadcrumbExample" -Content {
        New-UDBreadcrumbItem -Link "/Example"-LinkText "Example" -Icon "helicopter" -Active $true
        New-UDBreadcrumbItem -Link "/Home" -LinkText "Home" -icon "home"
        New-UDBreadcrumbItem -Link "/Links" -LinkText "Links" -icon "address_book"

    }
```

You will have to add this to each page you want the breadcrumb component to be displayed upon, but put the link to the page you are currently on as the first link in the list to get it to appear blue as active.  So for the home page it would be
```
New-UDPage -Name "Home" -Icon home -Content {
    New-UDBreadcrumb -iD "BChome" -Content {
        New-UDBreadcrumbItem -Link "/Home" -LinkText "Home" -icon "Home"  -Active $true
        New-UDBreadcrumbItem -Link "/Links" -LinkText "Links" -icon "address_book"
        New-UDBreadcrumbItem -Link "/Example" -LinkText "Example" -Icon "helicopter"
    }
    New-UDCard -Title "This is the home page"
}
```

## Again you need both modules for this to work
