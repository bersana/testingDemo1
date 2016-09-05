<?php
namespace AppBundle;
use AppBundle\UnitTester;

class UserCest
{
    public function _before(UnitTester $I)
    {
    }

    public function _after(UnitTester $I)
    {
    }

    // tests
    public function validateUser(UnitTester $I)
    {
		  $user = $I->createUser();
        $user->username = null;
        $I->assertFalse($user->validate(['username']); 

        $user->username = 'toolooooongnaaaaaaameeee';
        $I->assertFalse($user->validate(['username']));

        $user->username = 'anna_admin';
        $I->assertTrue($user->validate(['username']));

        $I->seeInDatabase('users', ['name' => 'anna_admin']);
    }
}
