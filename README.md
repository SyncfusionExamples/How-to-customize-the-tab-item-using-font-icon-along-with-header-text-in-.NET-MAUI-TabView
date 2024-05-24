**Overview**

When working with the [.NET MAUI TabView](https://www.syncfusion.com/maui-controls/maui-tab-view), you can enhance the user interface by adding font icons to the TabItems along with header text. This can be achieved by using the `FontImageSource` element within your XAML code. Below is a step-by-step guide on how to customize your TabItems with font icons.

**Adding Font Icons to TabItems**

To add font icons to your TabItems, you will need to use the `FontImageSource` element within each `SfTabItem`. Here's an example of how to do this:

```xml
<tabView:SfTabView x:Name="tabView" TabBarBackground="HotPink">
    <tabView:SfTabView.Items>
        <!-- TabItem with a Call icon -->
        <tabView:SfTabItem Header="Call" x:Name="callItem" ImagePosition="Left">
            <tabView:SfTabItem.ImageSource>
                <FontImageSource Glyph="&#xfeb6;" x:Name="call"
                                 Color="{Binding Source={x:Reference callItem},Path=TextColor}"
                                 FontFamily="MaterialDesignIcons"/>
            </tabView:SfTabItem.ImageSource>
            <!-- Content for the Call tab -->
            <!-- ... -->
        </tabView:SfTabItem>

        <!-- TabItem with a Favourite icon -->
        <tabView:SfTabItem Header="Favourite" x:Name="favItem" ImagePosition="Left">
            <tabView:SfTabItem.ImageSource>
                <FontImageSource Glyph="&#xf2d1;" x:Name="fav"
                                 Color="{Binding Source={x:Reference favItem},Path=TextColor}"
                                 FontFamily="MaterialDesignIcons"/>
            </tabView:SfTabItem.ImageSource>
            <!-- Content for the Favourite tab -->
            <!-- ... -->
        </tabView:SfTabItem>

        <!-- TabItem with a Contacts icon -->
        <tabView:SfTabItem Header="Contacts" x:Name="contactsItem" ImagePosition="Left">
            <tabView:SfTabItem.ImageSource>
                <FontImageSource Glyph="&#xf6ca;" x:Name="contacts"
                                 Color="{Binding Source={x:Reference contactsItem},Path=TextColor}"
                                 FontFamily="MaterialDesignIcons"/>
            </tabView:SfTabItem.ImageSource>
            <!-- Content for the Contacts tab -->
            <!-- ... -->
        </tabView:SfTabItem>
    </tabView:SfTabView.Items>
</tabView:SfTabView>
```

In the above example, each `SfTabItem` has an `ImageSource` defined with a `FontImageSource`. The `Glyph` attribute is used to specify the icon, and the `Color` attribute is bound to the `TextColor` of the tab item, ensuring that the icon color matches the text color. The `FontFamily` should be set to the font that contains your icons, such as "MaterialDesignIcons" in this case.

**Binding the Icon Color**

To ensure that the icon color matches the text color of the tab, a binding is set up to reference the `TextColor` property of the `SfTabItem`. This is done using the `{Binding Source={x:Reference NameOfTabItem}, Path=TextColor}` syntax.

**Output**

![TabView.gif](https://support.syncfusion.com/kb/agent/attachment/article/16148/inline?token=eyJhbGciOiJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGRzaWctbW9yZSNobWFjLXNoYTI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjIzMjg4Iiwib3JnaWQiOiIzIiwiaXNzIjoic3VwcG9ydC5zeW5jZnVzaW9uLmNvbSJ9.6eV4XcYEXFVpu_dQvojG0xoORaJlB11x39K7ZJUVfIk)