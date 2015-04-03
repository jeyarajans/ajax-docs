---
title: OnEnable
page_title: OnEnable | UI for ASP.NET AJAX Documentation
description: OnEnable
slug: input/client-side-programming/events/onenable
tags: onenable
published: True
position: 5
---

# OnEnable



## 

The __OnEnable__ client-side event handler is called when the input control is enabled.

>note The __OnEnable__ event is supported by all __RadInput__ controls.
>


Two parameters are passed to the event handler:

* __sender__ is the input control.

* __eventArgs__ is an instance of [Sys.EventArgs](http://www.asp.net/AJAX/Documentation/Live/ClientReference/Sys/EventArgsClass/default.aspx).

The following example uses the __OnEnable__ event to disable another control when the input control is enabled:

````ASPNET
	    <telerik:RadTextBox ID="RadTextBox1" runat="server" ShowButton="True">
	        <ClientEvents OnEnable="DisableOtherInput" OnButtonClick="ToggleEnabled" />
	    </telerik:RadTextBox>
	    <telerik:RadNumericTextBox ID="RadNumericTextBox1" runat="server" Enabled="False" ShowButton="True">
	            <ClientEvents onenable="DisableOtherInput" onbuttonclick="ToggleEnabled" />
	    </telerik:RadNumericTextBox>
````



````JavaScript
	    <script type="text/javascript">
	        function DisableOtherInput(sender, eventArgs)
	        {
	            if (sender.get_id() == "<%= RadTextBox1.ClientID %>")
	            {
	                var other = $find("<%= RadNumericTextBox1.ClientID %>");
	                other.disable();
	            }
	            else if (sender.get_id() == "<%= RadNumericTextBox1.ClientID %>")
	            {
	                var other = $find("<%= RadTextBox1.ClientID %>");
	                other.disable();
	            }
	        }
	        function ToggleEnabled(sender, eventArgs)
	        {
	            if (sender.get_enabled()) sender.enable();
	            else sender.enable();
	        }
	    </script>
````



# See Also

 * [OnDisable]({%slug input/client-side-programming/events/ondisable%})