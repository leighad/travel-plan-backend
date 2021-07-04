##  **MODELS**

### *USER*
#### ->Attributes
* username
* email
* password
<br>

#### ->Relationships
* <small>has_many :trips</small><br>
* <small>has_many :destinations, through: :trips</small>
<br><br>

### *LOCATION*
#### ->Attributes
* city
* state/province/region
* country
<br>

#### ->Relationships
* <small>has_many :destinations</small>
<br><br>

### *DESTINATION*
#### ->Attributes
* name
* description
<br>

#### ->Relationships
* <small>belongs_to :location</small>
<br><br>

### *COMMENT*
#### ->Attributes
* content
<br>

#### ->Relationships
* <small>belongs_to :user</small><br>
* <small>belongs_to :destination</small>
<br><br>

### *TRIP*
#### ->Attributes
* date(s)
<br>

#### ->Relationships
* <small>belongs_to :user</small><br>
* <small>belongs_to :destination</small>
* <small>has_many :destinations</small>?
<br><br>
