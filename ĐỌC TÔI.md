#import "APIClient.h"

void function(){
    APIClient *API = [[APIClient alloc] init];
    [API setToken:@"TOKEN"]; //Enter token from dashboard
   //paid
    [API paid:^{
        //load menu
        loadview(); //etc
        menuSetup();

        //Optional
    	NSLog(@"APIData - Key: %@", [API getKey]);
        NSLog(@"APIData - UDID: %@", [API getUDID]);
        NSLog(@"APIData - Expiry date: %@", [API getExpiryDate]);
        NSLog(@"APIData - Device model: %@", [API getDeviceModel]);

   }];
}
