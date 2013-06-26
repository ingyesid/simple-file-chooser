simple-file-chooser
===================

Little library for choose file from SDCard in android 2.2+


![Home](https://lh3.googleusercontent.com/-XLVxaf-tnPw/UcmiOwKfcAI/AAAAAAAADAw/X_NteRUpEf8/w353-h588-no/Screenshot_2013-06-25-08-54-51.png)
![Home](https://lh4.googleusercontent.com/-tIBtXwWYBFc/Ucmh3spd_HI/AAAAAAAADAg/roDEoDXCrA4/w353-h588-no/Screenshot_2013-06-25-08-54-59.png)
![Home](https://lh4.googleusercontent.com/-KbvA3s1oGHU/UcmiOAerEEI/AAAAAAAADAo/GTG9fUKh5QI/w353-h588-no/Screenshot_2013-06-25-08-54-42.png)


HOW TO USE
===================
-- Add the library reference to your project --


<code> public class MainActivity extends Activity {

	final int FILE_CHOOSER=1; 
	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		Intent intent = new Intent(MainActivity.this, FileChooserActivity.class);
		startActivityForResult(intent, FILE_CHOOSER);
	}

	@Override
	public boolean onCreateOptionsMenu(Menu menu) {
		
		getMenuInflater().inflate(R.menu.main, menu);
		return true;
	}
	@Override
	public void onActivityResult(int requestCode, int resultCode, Intent data) {
	    if ((requestCode == FILE_CHOOSER) && (resultCode == RESULT_OK)) {
	        String fileSelected = data.getStringExtra(Constants.KEY_FILE_SELECTED);
	        Toast.makeText(this, "file selected "+fileSelected, Toast.LENGTH_SHORT).show();
	    }                   
	}

}

</code> 