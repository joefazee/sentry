### Finding Groups

Sentry provides simple methods to find you your groups.

----------

#### Exceptions

##### Cartalyst\Sentry\Groups\GroupNotFoundException

If the provided group was not found, this exception will be thrown.

----------

#### Find all the Groups

This will return all the groups.

##### Example

	$groups = Sentry::getGroupProvider()->findAll();

----------

#### Find a group by it's ID.

Find a group by it's ID.

##### Example

	try
	{
		$group = Sentry::getGroupProvider()->findById(1);
	}
	catch (Cartalyst\Sentry\Groups\GroupNotFoundException $e)
	{
		echo 'Group not found.';
	}

----------

#### Find a Group by it's Name

Find a group by it's name.

####Example

	try
	{
		$group = Sentry::getGroupProvider()->findByName('admin');
	}
	catch (Cartalyst\Sentry\Groups\GroupNotFoundException $e)
	{
		echo 'Group not found.';
	}
