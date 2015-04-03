---
title: RTL support
page_title: RTL support | UI for ASP.NET AJAX Documentation
description: RTL support
slug: panelbar/appearance-and-styling/rtl-support
tags: rtl,support
published: True
position: 10
---

# RTL support



## 

__RadPanelBar__ includes support for right-to-left locales using the direction attribute. If you set __dir="rtl"__ on the __RadPanelBar__ object or on any parent HTML element, __RadPanelBar__ changes the position of the text that appears on items:

![RTL](images/panelbar_rtl.png)

>note Image position is still controlled by the __ImagePosition__ property.
>


````ASPNET
	     
		<telerik:RadPanelBar
	       ID="RadPanelBar1" runat="server"
	       Skin="Office2010Silver"
	       dir="rtl">
	     <Items>
	       <telerik:RadPanelItem runat="server" Text="One" >
	         <Items>
	           <telerik:RadPanelItem runat="server" Text="i" />
	           <telerik:RadPanelItem runat="server" Text="ii" />
	           <telerik:RadPanelItem runat="server" Text="iii" />
	         </Items>
	       </telerik:RadPanelItem>
	       <telerik:RadPanelItem runat="server" Text="Two" >
	         <Items>
	           <telerik:RadPanelItem runat="server" Text="1" />
	           <telerik:RadPanelItem runat="server" Text="2" />
	         </Items>
	       </telerik:RadPanelItem>
	       <telerik:RadPanelItem runat="server" Text="Three">
	         <Items>
	           <telerik:RadPanelItem runat="server" Text="a" />
	           <telerik:RadPanelItem runat="server" Text="b" />
	         </Items>
	       </telerik:RadPanelItem>
	     </Items>
	    </telerik:RadPanelBar> 
				
````



# See Also

 * [Adding Images to Items]({%slug panelbar/appearance-and-styling/adding-images-to-items%})