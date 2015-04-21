# Payeezy bindings for WebBased app

Sample code provide Payeezy Javascript Integration

![alt tag](https://github.com/payeezy/payeezy_js/raw/master/example/payeezyjs.png)

1. Payeezy.js (which is included on the page using a &lt; script> tag) intercepts the form submit, and then
asynchronously posts the credit card details to Payeezy. This call uses JSONP over https, passing in API key and an
identifier– trtoken. Both of these values are provisioned for the merchant‘s developer via the developer portal.
2. On success Payeezy returns a one-time use token (type=payeezy) to payeezy.js. Payeezy.js saves the pertinent
token information in a hidden form field on the checkout form. Failure messages are returned in the response,
which can be handled as appropriate.
3. Payeezy.js then submits the form with the hidden token along with other form info to the merchant server. The
credit card related fields that were used for tokenization are stripped out of the form i.e. the merchant server never
4. Merchants server submits the token to Payeezy to complete the transaction using the appropriate server side
library (optional to use but recommended). This API call uses HMAC authentication, over https. Refer to the
Payeezy developer portal – API Docs and Sandbox section to know more.
5. Payeezy completes the transaction with the provided token (authorization, purchase). The response contains a
new token to use for the related secondary transaction (capture, void, refund). Success/failure message is handled
accordingly by the merchant’s server

For more details on 'Payeezy JS' example refer [payeezy_js example](../../tree/master/example)

For more details on 'Payeezy JS Guide' refer [payeezy_js guide](../../blob/master/guide/payeezy_js042015.pdf)

# Getting Started with Payeezy
Using below listed steps, you can easily integrate your mobile/web payment application with Payeezy APIs and go LIVE!
*	LITE  - REGISTRATION  
*	GET CERTIFIED
*	ADD MERCHANTS 
*	LIVE!

![alt tag](https://github.com/payeezy/get_started_with_payeezy/raw/master/payeezy_flow_diagram.png)

For more information on getting started, visit  [get_start_with_payeezy guide] (https://github.com/payeezy/get_started_with_payeezy/blob/master/get_started_with_payeezy042015.pdf) or [download](https://github.com/payeezy/get_started_with_payeezy/raw/master/get_started_with_payeezy042015.pdf)

# Testing - Payeezy {SANDBOX region}
For test credit card,eCheck,GiftCard please refer to [test data ](https://github.com/payeezy/testing_payeezy/blob/master/payeezy_testdata042015.pdf) or [download] (https://github.com/payeezy/testing_payeezy/raw/master/payeezy_testdata042015.pdf)

# Error code/response - Payeezy {SANDBOX/PROD region}
For HTTP status code, API Error codes and error description please refer to [API error code ](https://developer.payeezy.com/payeezy_new_docs/apis) and select your API

#Questions?
We're always happy to help with code or other questions you might have! Check out [FAQ page](https://developer.payeezy.com/faq-page) or call us. 

## Contributing

1. Fork it 
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request  

## Feedback

Payeezy JS is in active development. We appreciate the time you take to try it out and welcome your feedback!
Here are a few ways to get in touch:
* [GitHub Issues](https://github.com/payeezy/payeezy/issues) - For generally applicable issues and feedback
* support@payeezy.com - for personal support at any phase of integration
* [1.855.799.0790](tel:+18557990790)  - for personal support in real time 

## Terms of Use

Terms and conditions for using Payeezy JavaScript: Please see [Payeezy Terms & conditions](https://developer.payeezy.com/terms-use)
 
### License
The Payeezy JavaScript is open source and available under the MIT license. See the LICENSE file for more info.
