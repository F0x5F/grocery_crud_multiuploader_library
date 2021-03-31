# Grocery Crud Multiuploader library
Addon for Grocery CRUD library, select and load multiple files

# Tested CI v.3.x -> GC v.1.5.x

### Usage
```php 
$crud->new_multi_upload(arg1,arg2);
         arg1 - string, field_name
         arg2 - array, upload field settings
```

```php 
class Your_class extends CI_Controller {

function __construct()
{
	parent::__construct();
	$this->load->database();
	$this->load->library('grocery_CRUD');
    	$this->load->library('Grocery_CRUD_Multiuploader');
}

/* Upload field configuration, path, allowed type etc */
$config = array(
		    /* Destination directory */
		    "path_to_directory"       =>'assets/multiuploader/uploads/files/',
		    /* Allowed upload type */
		    "allowed_types"           =>'gif|jpeg|jpg|png',
		    /* Show allowed file types while editing ? */
		    "show_allowed_types"      => true,
			/* No file text */
		    "no_file_text"            =>'No files',
			/* enable full path or not for anchor during list state */
		     "enable_full_path"        => false,
		    /* Download button will appear during read state */
		    "enable_download_button"  => true,
		    /* show download button only for this types...*/
		    "download_allowed"        => 'jpg' 		
			);
$crud->new_multi_upload("files",$config);
```

#### Screenshots
![Add files][1]

[1]:https://github.com/F0x5F/grocery_crud_multiuploader_library/blob/main/screenshots/srcreen_1.png
