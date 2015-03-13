
## Usage

You can create an utility class where you can define your application credentials, like the one below:

		public class ApplicationData {
			public static final String CLIENT_ID = "";
			public static final String CLIENT_SECRET = "";
			public static final String CALLBACK_URL = "";
		}

To instantiage the main class for the oauth flow, you need to follow the code below:

		InstagramApp mApp; = new InstagramApp(this, 
			ApplicationData.CLIENT_ID, 
			ApplicationData.CLIENT_SECRET, 
			ApplicationData.CALLBACK_URL);

Once you have the main class ready for the authorization, you can start the authorization flow by calling the following method:

		mApp.authorize();

If you token is expired, you can call this method to refresh it:

		mApp.refreshToken();

To get the account list, call the following method

		mApp.getAccountList();


