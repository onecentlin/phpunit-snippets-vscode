# PHPUnit Snippets

PHPUnit assertion and test snippets support for Visual Studio Code.

## Screenshot

![Demo](https://github.com/onecentlin/phpunit-snippets-vscode/raw/master/images/screenshots.gif)

## Snippet Trigger

### Assertion

Start with `assert:` and follows support assertion.

For example: Type `assert:Equals` trigger with tab key, it produces `$this->assertEquals($expected, $actual);` snippet for you.

| Trigger                            | Snippet                                     |
|------------------------------------|---------------------------------------------|
| assert:ArrayHasKey                 |  $this->assertArrayHasKey()                 |
| assert:ClassHasAttribute           |  $this->assertClassHasAttribute()           |
| assert:ArraySubset                 |  $this->assertArraySubset()                 |
| assert:ClassHasStaticAttribute     |  $this->assertClassHasStaticAttribute()     |
| assert:Contains                    |  $this->assertContains()                    |
| assert:ContainsOnly                |  $this->assertContainsOnly()                |
| assert:ContainsOnlyInstancesOf     |  $this->assertContainsOnlyInstancesOf()     |
| assert:Count                       |  $this->assertCount()                       |
| assert:DirectoryExists             |  $this->assertDirectoryExists()             |
| assert:DirectoryIsReadable         |  $this->assertDirectoryIsReadable()         |
| assert:DirectoryIsWritable         |  $this->assertDirectoryIsWritable()         |
| assert:Empty                       |  $this->assertEmpty()                       |
| assert:EqualXMLStructure           |  $this->assertEqualXMLStructure()           |
| assert:Equals                      |  $this->assertEquals()                      |
| assert:False                       |  $this->assertFalse()                       |
| assert:FileEquals                  |  $this->assertFileEquals()                  |
| assert:FileExists                  |  $this->assertFileExists()                  |
| assert:FileIsReadable              |  $this->assertFileIsReadable()              |
| assert:FileIsWritable              |  $this->assertFileIsWritable()              |
| assert:GreaterThan                 |  $this->assertGreaterThan()                 |
| assert:GreaterThanOrEqual          |  $this->assertGreaterThanOrEqual()          |
| assert:Infinite                    |  $this->assertInfinite()                    |
| assert:InstanceOf                  |  $this->assertInstanceOf()                  |
| assert:InternalType                |  $this->assertInternalType()                |
| assert:IsReadable                  |  $this->assertIsReadable()                  |
| assert:IsWritable                  |  $this->assertIsWritable()                  |
| assert:JsonFileEqualsJsonFile      |  $this->assertJsonFileEqualsJsonFile()      |
| assert:JsonStringEqualsJsonFile    |  $this->assertJsonStringEqualsJsonFile()    |
| assert:JsonStringEqualsJsonString  |  $this->assertJsonStringEqualsJsonString()  |
| assert:LessThan                    |  $this->assertLessThan()                    |
| assert:LessThanOrEqual             |  $this->assertLessThanOrEqual()             |
| assert:Nan                         |  $this->assertNan()                         |
| assert:Null                        |  $this->assertNull()                        |
| assert:ObjectHasAttribute          |  $this->assertObjectHasAttribute()          |
| assert:RegExp                      |  $this->assertRegExp()                      |
| assert:StringMatchesFormat         |  $this->assertStringMatchesFormat()         |
| assert:StringMatchesFormatFile     |  $this->assertStringMatchesFormatFile()     |
| assert:Same                        |  $this->assertSame()                        |
| assert:StringEndsWith              |  $this->assertStringEndsWith()              |
| assert:StringEqualsFile            |  $this->assertStringEqualsFile()            |
| assert:StringStartsWith            |  $this->assertStringStartsWith()            |
| assert:That                        |  $this->assertThat()                        |
| assert:True                        |  $this->assertTrue()                        |
| assert:XmlFileEqualsXmlFile        |  $this->assertXmlFileEqualsXmlFile()        |
| assert:XmlStringEqualsXmlFile      |  $this->assertXmlStringEqualsXmlFile()      |
| assert:XmlStringEqualsXmlString    |  $this->assertXmlStringEqualsXmlString()    |

### Incomplete and Skipped Test

| Trigger             | Snippet                      |
|---------------------|------------------------------|
| mark:TestIncomplete |  $this->markTestIncomplete() |
| mark:TestSkipped    |  $this->markTestSkipped()    |

### Expect Exception

| Trigger                    | Snippet                               |
|----------------------------|---------------------------------------|
| exp:Exception              | $this->expectException()              | 
| exp:ExceptionCode          | $this->expectExceptionCode()          |
| exp:ExceptionMessage       | $this->expectExceptionMessage()       |
| exp:ExceptionMessageRegExp | $this->expectExceptionMessageRegExp() |

### Test Snippets

Start with `pu:` and follows support code completion.

| Trigger                    | Snippet                                       |
|----------------------------|-----------------------------------------------|
| pu:testCase                | Create basic test case class                  | 
| pu:setUp                   | setUp()                                       |
| pu:tearDown                | tearDown()                                    |
| pu:testFunction            | Create base test function                     |
| pu:testDoxFunction         | Create test function with @testdox annotation |
| pu:testException           | Create test function with @expectedException  |

#### Examples

Trigger: `pu:testCase`

```php
use PHPUnit\Framework\TestCase;

/**
 * ClassNameTest
 * @group group
 */
class ClassNameTest extends TestCase
{
    /** @test */
    public function test_function()
    {
        // Test
    }
}
```

Trigger: `pu:setUp`

```php
public function setUp()
{
    // setup
}
```

Trigger: `pu:tearDown`

```php
public function tearDown()
{
    // unset
}
```

Trigger: `pu:testFunction`

```php
/** @test */
public function test_function()
{
    // Test    
}
```

Trigger: `pu:testDoxFunction`

```php
/** 
 * @test
 * @testdox  description
 */
public function test_function()
{
    // Test    
}
```

Trigger: `pu:testException`

```php
/** 
 * @test
 * @expectedException  exception
 */
public function test_function()
{
    // Test
}
```

**Enjoy Unit Testing!!**