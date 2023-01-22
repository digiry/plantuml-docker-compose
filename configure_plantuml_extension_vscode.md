# Configure PlantUML extension in VSCode

VSCode extension:  `jebbs.plantuml`

Once you have been run the plantuml docker on your local, you should configure the settings in VSCode.

<br>

## How to configure

In `settings.json`, types the following settings for `plantuml`.

```yaml
  "plantuml.render": "Local",
  "plantuml.server": "http://localhost:8080",
```

Create a markdown file, then insert the sample plantuml markdown.

````plain
```plantuml
@startuml

start
:User Submits Order;
if (Check Warehouse Stock?) then (In Stock)
    if (Process Payment) then (Payment Success)
        if (Dispatch Order) then (Dispatch Success)
            :Show Success;
        else (Dispatch Failed)
            :Show Error;
        endif
    else (Payment Failed)
        :Show Error;
    endif
else (No Stock)
    :Show Error;
endif

stop

@enduml
```
````

If you open the markdown preview, the preview will be blocked and then some button will be displayed on top.

Button: `Some content has been disabled in this document`

Once you click the button, you can see the Markdown Security menu.

![Blocked Preview images](res/Blocked_plantuml_preview.png)

Choose the option you want.

I chose the `Allow insecure local content` option.

![Selecting Markdown Security settings](res/Menus_markdown_security_settings.png)

After done, you can see the renedered plantuml preview.

![Allowed Insecure Local Contents](res/Allowed_Insecure_local_contents.png)
