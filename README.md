# FSL.ButtonBorderAndRadiusInXamarinForms

**Button Border and Radius in Xamarin Forms**

f you program on ASP.NET Web Forms or even pure HTML you know when you need to change button border is very very very easy.

![enter image description here](https://fabiosilvalima.files.wordpress.com/2016/11/custom-button-border.png)

BUT, in Xamarin Forms it’s another world.

It’s become simple when you already know the solution..

---

What is in the source code?
---

#### <i class="icon-file"></i> FSL.ButtonBorderAndRadiusInXamarinForms

- Visual Studio solution file;
- Portable application;
- iOS and Android application;
- Android Button Custom Renderer Class; 

> **Remarks:**

> - You can download and run that application no problem. If you need to install and configure Xamarin, please check my other [post here][1].

---

What is the goal?
---

Create a button using XAML to draw a rounded red border like that:

![enter image description here](https://fabiosilvalima.files.wordpress.com/2016/11/withcustomrender1.png?w=616)

**Assumptions:**
- I am using XAML for simplicity. You don't need to know XAML at this point.


Source code...
---

**FlatButtonRenderer.cs**
```csharp
using Xamarin.Forms.Platform.Android;
using Xamarin.Forms;
 
[assembly: ExportRenderer(typeof(Button), typeof(FSL.XF1.Droid.FlatButtonRenderer))]
namespace FSL.XF1.Droid
{
    public class FlatButtonRenderer : ButtonRenderer
    {
        protected override void OnDraw(Android.Graphics.Canvas canvas)
        {
            base.OnDraw(canvas);
        }
 
        protected override void OnElementChanged(ElementChangedEventArgs<Button> e)
        {
            base.OnElementChanged(e);
        }
    }
}
```

**MainPage.xaml**
```xml
<Button Text="Click Me"         
TextColor="Red"
BackgroundColor="White"
BorderColor="Red"
BorderWidth="1"
BorderRadius="3"
VerticalOptions="Center"
HorizontalOptions="Center">
</Button>
```



References:
---

- Visual Studio 2015 Xamarin Forms Install and Config [check here][1];

Licence:
---

- [Licence MIT][4]


  [1]: https://fabiosilvalima.wordpress.com/2016/11/10/visual-studio-2015-xamarin-forms-install-and-config/
