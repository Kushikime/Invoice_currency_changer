DOWNLOAD MODULE : https://github.com/Kushikime/Invoice_currency_changer/blob/master/saleorder_currency_exchanger.rar



<h2>When i hit "Create Invoice" button on sale order, odoo open for us a wizard where we can choose some option's.</h2>
<img src="https://github.com/Kushikime/Invoice_currency_changer/blob/master/Create_invoice_button.png" width="400">

<img src="https://github.com/Kushikime/Invoice_currency_changer/blob/master/Create_invoice_wizard.png" width="480">

<h2>Then if we hit "Create Invoices" odoo will create an invoice.</h2>
<img src="https://github.com/Kushikime/Invoice_currency_changer/blob/master/example_of_invoice.png" width="480">

<h3>The problem here is that, when somebody will check box "Convert to base currency",
the Invoice must take current base currency of the system, in my case it's (USD),
then re-calculate the values for each item, and update invoice with new values.</h3>

<h1>My plan:
	
<h3>1.First try to modify the _create_invoice method of  "SaleAdvancePaymentInv" and update the currency to default, if the box is checked.</h3>

<h3>2.When i hit checkbox field that will show 2 variant's of converting:</h3>
	<img src="https://github.com/Kushikime/Invoice_currency_changer/blob/master/checkbox_hitted.png" width="400"><br/><hr/>
	<h4>a)Use last currency:<br/><img src="https://github.com/Kushikime/Invoice_currency_changer/blob/master/checkbox_first.png" width="400"></h4><br/><hr/>
	<h4>b)Enter my currency:<br/><img src="https://github.com/Kushikime/Invoice_currency_changer/blob/master/checkbox_second.png" width="400"></h4><hr/>

		
<h3>In first case system use the currency for the currency which in the Sale Order.
(*the values of currency rate i get from the currency_management)</h3><br/><hr/>
<img src="https://github.com/Kushikime/Invoice_currency_changer/blob/master/first_checbox_value.png" width="480">
<h3>In second case we can enter our currency, and system will use this to calculate new prices of products</h3>
		
