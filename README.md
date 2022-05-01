# CPF.Validation.Attribute

A simple attribute validation for Brazil's Individual Taxpayer Registry.

## Example

 in Entity:

~~~c#

public class People
    {
        public string Name { get; set; }

        [Cpf]
        public string Cpf { get; set; }

        public string Email { get; set; }

        //...

    }

~~~

in Controller:

~~~c#

//...

[HttpPost]
public IActionResult PostPeople([FromBody] People people)
{
    if (!ModelState.IsValid)
        return BadRequest();

    ///...
}

//...
~~~
