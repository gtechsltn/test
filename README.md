# Test

# Git
```
echo "# Test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M master
git remote add origin https://github.com/gtechsltn/test.git
git push -u origin master
```

## Fragile tests
```
[Test]
public void UserServiceShouldActivateUser()
{
  //Arrange
  var user = new User();
  var userStoreFake = new UserStoreFake(user);

  var userService = new UserService(userStoreFake);

  //Actual
  userService.Activate(user);

  //Assert
  user = userStoreFake.Users.First();
  Check.That(user.IsActive).IsTrue();
}
```

## Eager tests
```
[Test]
public void ActiveAccountShouldBeInitialized_WhenConstructed()
{
  ...
}
[Test]
public void ShouldIncreaseBalance_WhenDepositIsMade()
{
  ...
}
[Test]
public void ShouldReturnError_WhenWithdrawAmountExceedsBalance()
{
  ...
}
[Test]
public void ShouldDecreaseBalance_WhenValidWithdrawIsMade()
{
  ...
}
```

## Mistery Guest
```
[Test]
public void ContractShouldCombineNameAndAddress()
{
  //Arrange
  var user = new User
  {
    FirstName = "John",
    LastName = "Smith",
    Address = new Address
    {
      Stree = "123 Main St",
      City = "Springfield",
      ZipCode = "12345"
    }
  };

  //Actual
  var contract = user.GetContract();

  //Assert
  contract.Should().Be("John Smith, 123 Main St, Springfield, 12345");
}
```

## AAA
```
[Test]
public void UserServiceShouldActivateUser()
{
  //Arrange

  //Actual

  //Assert

}
```
