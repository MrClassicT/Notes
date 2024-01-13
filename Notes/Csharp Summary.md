# Cs Samenvatting
- [[#Notes|Notes]]
		- [[#Access modifiers|Access modifiers]]
		- [[#Variables|Variables]]
		- [[#Constants|Constants]]
		- [[#Read-only|Read-only]]
		- [[#Static|Static]]
		- [[#Ref|Ref]]
		- [[#Out|Out]]
		- [[#Destructor|Destructor]]
		- [[#Subclass definition|Subclass definition]]
				- [[#base|base]]
				- [[#Virtual|Virtual]]
				- [[#Override|Override]]
		- [[#List|List]]
		- [[#Collection|Collection]]
			- [[#Collection#IList\<T>|IList\<T>]]
			- [[#Collection#Collection interfaces|Collection interfaces]]
		- [[#Entity vs Value Object|Entity vs Value Object]]
		- [[#Unit Testing|Unit Testing]]
	- [[#Notes#Blazor|Blazor]]
		- [[#Blazor#Client Side (WASM)|Client Side (WASM)]]
			- [[#Client Side (WASM)#Voordelen|Voordelen]]
			- [[#Client Side (WASM)#Nadelen|Nadelen]]
		- [[#Blazor#Server side|Server side]]
			- [[#Server side#Voordelen|Voordelen]]
			- [[#Server side#Nadelen|Nadelen]]
		- [[#Blazor#Onderdelen|Onderdelen]]
			- [[#Onderdelen#Structuur|Structuur]]
		- [[#Blazor#Fakers|Fakers]]
			- [[#Fakers#Implementatie|Implementatie]]
	- [[#Notes#Rest|Rest]]
	- [[#Notes#DTO: Data Transfer Object|DTO: Data Transfer Object]]
		- [[#DTO: Data Transfer Object#Validator|Validator]]
		- [[#DTO: Data Transfer Object#Middleware|Middleware]]
	- [[#Notes#In het kort|In het kort]]
	- [[#Notes#Images|Images]]
	- [[#Notes#Filter|Filter]]
	- [[#Notes#Entity Base class|Entity Base class]]
	- [[#Notes#Configuration grouping|Configuration grouping]]
	- [[#Notes#Lifetime|Lifetime]]
	- [[#Notes#[Triggers](https://hogent-web.github.io/csharp/chapters/09/slides/index.html#27)|[Triggers](https://hogent-web.github.io/csharp/chapters/09/slides/index.html#27)]]
	- [[#Notes#Effectieve db gebruiken (sqlserver)|Effectieve db gebruiken (sqlserver)]]
	- [[#Notes#Overriding default conventions|Overriding default conventions]]
	- [[#Notes#Triggered package output|Triggered package output]]
	- [[#Notes#Default values for entities|Default values for entities]]
		- [[#Default values for entities#Column name aanpassen (change column name)|Column name aanpassen (change column name)]]
			- [[#Column name aanpassen (change column name)#OwnsOne / OwnsMany VS HasOne/HasMany|OwnsOne / OwnsMany VS HasOne/HasMany]]
		- [[#Default values for entities#Ervoor zorgen dat alles mapped is.|Ervoor zorgen dat alles mapped is.]]
		- [[#Default values for entities#Tracking vs. No-tracking|Tracking vs. No-tracking]]
		- [[#Default values for entities#Loading (related) data|Loading (related) data]]
			- [[#Loading (related) data#Update|Update]]
			- [[#Loading (related) data#Verwijderen (delete)|Verwijderen (delete)]]
			- [[#Loading (related) data#Meerdere veranderingen tegelijkertijd. (multiple operations)|Meerdere veranderingen tegelijkertijd. (multiple operations)]]
		- [[#Default values for entities#Dapper VS EFC|Dapper VS EFC]]
			- [[#Dapper VS EFC#Dapper|Dapper]]
			- [[#Dapper VS EFC#Entity Framework Core|Entity Framework Core]]
	- [[#Notes#H10 - Authentication|H10 - Authentication]]
		 [[#H10 - Authentication#Iets afzonderen voor een bepaalde rol|Iets afzonderen voor een bepaalde rol]]
			 [[#Iets afzonderen voor een bepaalde rol#Pagina zelf|Pagina zelf]]
			 [[#Iets afzonderen voor een bepaalde rol#In de navigatie|In de navigatie]]
			 [[#Iets afzonderen voor een bepaalde rol#Backend - server/api|Backend - server/api]]
	  [[#Notes#H11 - Playwright testing|H11 - Playwright testing]]
		[[#H11 - Playwright testing#Managed vs Unmanaged|Managed vs Unmanaged]]
		  [[#H11 - Playwright testing#Levels of testing|Levels of testing]]
		  [[#H11 - Playwright testing#Testing|Testing]]
[[#Commands|Commands]]

---
# Notes
### Access modifiers
- **public**
- **private**
- **internal**: Only accessible within the same assembly (=unit of deployment, version control)
- **protected**: Only accessible within the class and all classes who inherit from this class. NOTE: Java = same package, but not in C#!
- **protected** **internal**: Combination of protected and internal.
- **Sealed**: no class may inherit from a given class. (**class only**)
- **Abstract**: When a class has one or more abstract methods. Can have both abstract and normal methods. But class MUST be implemented in order to create instance.
### Variables
Naming Convention: _camelCase
```cs
private string _accountNumber;
private decimal _balance;
```
### Constants
```cs
public const decimal WithdrawCost = 0.25M;
// M stands for Decimal, D is for double!!
```

### Read-only
```cs
private readonly string _accountNumber;
```

### Static
Always accessible, even without an instance of a class. They're linked to the class, not an instance!
```cs
private static int nrOfAccounts = 0;
```

A class can also be static. This means it can't be instantiated and everything in it is static as well. E.g. The 'Math' class. 
```cs
double result = Math.Cos(45);
```
### Ref
``` cs
public void Demonstrate1(BankAccount bankAccount)

{

bankAccount = null; // Change is only inside this scope.

}

public void Demonstrate2(ref BankAccount bankAccount)

{
// We change the actual object's property.
bankAccount = null;

}

BankAccount myAccount = new BankAccount();

Demonstrate1(myAccount); // myAccount won't be null, because the change is only in that method scope.

Demonstrate2(ref myAccount); // myAccount is null now, because the change has been made to the actual object we passed through.
```

### Out
Equal to Ref, except that the passed variable does not need to be instantiated. The usage is also the same, except that the keyword 'out' is used instead of 'ref'.

**Note**: We must assign a value to the 'out' parameter!

### Destructor
```cs
~BankAccount()
{/*Cleaning code here*/}
// a destructor: used for garbage collector, usually not needed.
```

### Subclass definition
class SubClassName : SuperClass { ... }
```cs
public class SavingsAccount : BankAccount { /* ... */ }
```

##### base 
Call a superclass constructor with base
```cs
public SavingsAccount(string accountNumber, decimal intrestRate)

: base(accountNumber) // call constructor of SuperClass BankAccount

{
```

##### Virtual
> So that subclasses can use [[#Override[|Override]]
```cs
public virtual void Withdraw(decimal amount)

{

_transactions.Add(new Transaction(amount, TransactionType.Withdraw));

Balance -= amount;

}
```

##### Override 
> In order to use this, you must use [[#Virtual|Virtual]] in you superclass.
```cs
public override void Withdraw(decimal amount)

{

base.Withdraw(amount);

base.Withdraw(WithdrawCost);

}
```

### List
```cs
// Short way to create a list

IEnumerable<string> list = new List<string>

{

"Monday", "Tuesday", "Wednesday", "Thursday", "Friday",

"Saturday", "Sunday"

}
```

### Collection
```cs
ICollection<string> list = new List<string>

{

"Monday", "Tuesday", "Wednesday", "Thursday", "Friday",

"Saturday", "Sunday"

}
```
Voordeel? - > Count en IsReadOnly methodes.
#### IList\<T>
> Implements ICollection\<T>
- Can **manipulate** its items
- **Index-based** access to the items (like an array)
    - first index is 0
    - use square brackets: \[index]
- Some useful methods:
    - Add(T item): int
    - Clear(): void
    - Insert(int index, T item): void
    - Remove(T item): void
    - RemoveAt(int index): void

#### Collection interfaces
![[Csharp_collection_Interfaces.png]]

---

### Entity vs Value Object

```csharp
// Entity 
public class Person
{
    public int Id { get; set; }
    public string Name { get; set; }
    public Address Address { get; set; }
}
 
// Value Object
public class Address
{
    public string City { get; set; }
    public string ZipCode { get; set; }
}
```

Entity is mutable, a value object isn't. Een persoon kan van adres veranderen, maar een adres gaat niet plots veranderen van waar deze locatie is.

Value objects zijn meer lightweight dan entiteiten. Deze zouden we dus altijd moeten prefereren indien er een keuze bestaat.


---
### Unit Testing
One Test class per unit.

`public void method Testing_Is_Optional()`

3A pattern: 
1) Arrange
2) Act
3) Assert


- **\[Fact\]** => Test with same data (one case)
- **\[Theory\]** => Data driven test (multiple cases at once)
	- **\[InlineData( \/\* input \*\/  )\]** => To give a parameter
		- Example:
		  ```csharp
public class BankAccountTest{

[Theory]
[InlineData("123-4567890-0333")] // too long
[InlineData("063-1547563@60")] // wrong format
[InlineData("133-4567890-03")] // not divisable by 97
public void NewAccount_WrongAccountNumber_Fails(string accountNumber)
  {
   // Assert
   Assert.Throws<ArgumentException>(() => new 
   BankAccount(accountNumber)));
  }
}
```
	- **\[MemberData(nameof( \/\* field \*\/))\]**
		- Example:
		```csharp
public class BankAccountTest{

  public static IEnumerable<object[]> TestData{
     get
		{
        DateTime yesterday = DateTime.Today.AddDays(-1);
        DateTime tomorrow = DateTime.Today.AddDays(1);
        yield return new object[] { null, null, 2 };
        yield return new object[] { yesterday, tomorrow, 2 };
        yield return new object[] { yesterday, yesterday, 0 };
        }
	}

	[Theory]
	[MemberData(nameof(TestData))]
public void GetTransactions_ReturnsTransactions(DateTime? from,
DateTime? till, int expected) { /* ... */ }
}
```

---

## Blazor
### Client Side (WASM)
#### Voordelen
- Draait op de client in de browser, deployable als statische bestanden.
- Blazor WASM functioneert offline en als Progressive Web App (PWA).
- Vermindert serverbelasting door op de client machine te draaien.

#### Nadelen
- Trager omdat .NET DLL's eerst gedownload moeten worden.
- Mono Framework interpreteert .NET Intermediate Language, wat trager is dan server-side Blazor.
- Werkt alleen op moderne browsers, is single-threaded.
- Niet SEO-vriendelijk zonder server-side rendering.

### Server side
#### Voordelen
- Render HTML-content vooraf, SEO-vriendelijk met snellere opstarttijd.
- Geen Web Assembly vereist en werkt op oudere browsers zoals IE 11.
- .NET code kan gedebugd worden in Visual Studio.

#### Nadelen
- Server start een in-memory sessie voor elke client, wat geheugen en CPU verbruikt.
- Werkt niet zonder internetverbinding en latency kan een probleem zijn bij veel events.

### Onderdelen
- Launchsettings.json
	- Enkel gebruikt bij development om profiel instellingen bij te houden.

- wwwroot
	- Statische assets die de browser kan downloaden.
	- bevat onder andere: css, fonts, favicon, ...

- Index.razor
	- de index pagina die de html variant overschrijdt.

- Mainlayout.razor
	- De layout pagina voor de applicatie. Kan aangepast worden.

- App.razor
	- Wordt geladen in de index.html
	- Layouts worden gedefineerd.
	- FocusOnNavigate kan gebruikt worden om de actieve pagina weer te geven in de navigatiebalk.
	
```cs
<Router AppAssembly="@typeof(App).Assembly">

	<Found Context="routeData">

		<RouteView RouteData="@routeData"

			DefaultLayout="@typeof(MainLayout)" />

		<FocusOnNavigate RouteData="@routeData" Selector="h1" />
	
	</Found>

	<NotFound>

		<PageTitle>Not found</PageTitle>

		<LayoutView Layout="@typeof(MainLayout)">

			<p>Sorry, there's nothing at this address.</p>

		</LayoutView>

	</NotFound>

</Router>
```

#### Structuur
> Blazor.Shared is niet bedoeld voor domein modelling!

Client => Blazor WASM client
Server => REST API
Shared => DTO's gedeeld, gedeeld met beide.

### Fakers

- **Dummy**: Eenvoudige objecten om methode signaturen te vullen, zonder actieve functie in tests.
- **Fake**: Hebben werkende implementaties maar zijn door shortcuts niet geschikt voor productie.
- **Stub**: Retourneren vaste waarden tijdens tests en reageren niet op niet-geprogrammeerde acties.
- **Spy**: Vergelijkbaar met stubs, maar registreren ook informatie over hun gebruik.
- **Mock**: Objecten met voorgeprogrammeerde verwachtingen die dienen als specificatie voor de verwachte interacties.
#### Implementatie
- Service laag waar de service de interface implement.
- Program.cs waar we Dependency injection doen: `builder.Services.AddScoped<IProductService, FakeProductService>();`
- Service interface dient op de Index.razor page (van `Products`) ge-inject worden.
```cs
  @page "/product"

@using Project.Shared.Products // ADDED

@inject IProductService ProductService // ADDED

<h1>Products</h1>
// ...
```

- Detail pagina voorbeeld.
```cs
// Using statements and directives here

@if (product == null)

{

<p><em>Loading...</em></p>

}

else

{

<h3>@product.Name</h3>

<p>@nameof(product.Id):@product.Id</p>

<p>@nameof(product.Description):@product.Description</p>

<p>@nameof(product.Price):@product.Price.ToString("C")</p>

<img src="@product.Image" alt="Some product img" width="100"/>

}
```

> Recommended exercise: [Blackjack](https://github.com/HOGENT-Web/csharp-ch-6-exercise-1)

---
## Rest
REpresentional State Transfer

REST is een architectuurstijl voor het ontwerpen van netwerktoepassingen, gebaseerd op stateless communicatie via het HTTP-protocol, met standaard operaties zoals POST, GET, PUT en DELETE, en het gebruik van Uniform Resource Identifiers (URI's) voor het adresseren van bronnen.

REST gebruikt 5 basisbeperkingen om te communiceren met webresources: een uniforme interface, een client-server architectuur, stateless, cacheerbaarheid, en een gelaagd systeem.

Uniforme interface: Alles is een resource.
	- fundamenteel concept van REST
	- heeft:
		- data
		- relaties met andere resources
		- methoden die ermee werken om data te raadplegen en aan te passen.


- URL: Uniform Resource Locator
- URI: Uniform Resource Indicator

Om te communiceren wordt gebruik gemaakt van representatie:
- Gebruik een mediatype
    - vaak JSON (`application/json`)
    - of XML (`application/xml`)
- Stel de juiste HTTP-headers in
    - Accept: wat verwacht je als invoer?
    - Content-Type: wat geef je terug?

Client - Server
	- Client en server moeten afzonderlijk kunnen evalueren.
	- Client moet alles kunnen doen met de beschikbare resource URI's

Stateless
	- Elke aanvraag is onafhankelijk
	- Server onthoudt vorige aanvragen en states niet.
	- Geen sessies of geschiedenissen.

Cacheable:
 - Alle antwoorden moeten cacheerbaar gemaakt worden indien nodig.
 - Goede caching verzekerd dat de server schaalbaar is.
 - Client antwoordt sneller.

Gelaagd systeem
	- REST staat toe om data en API te spreiden over meerdere servers
	- Voordeel: Servers kunnen onafhankelijk geschaald worden

HTTP status ranges:
- 1xx: Wachten, request ontvangen, proces voortzetten.
- 2xx: Alstublieft, request goed ontvangen, begrepen en geaccepteerd.
- 3xx: redirecting, verdere acties zijn nodig om de request te vervolledigen.
- 4xx: Fout, slechte syntax of request kan niet voldaan worden.
- 5xx: Fout, de server kan niet voldoen aan de (geldige) request.

-- Stukje over Documenteren overgeslagen, lijkt me overbodig voor examen? --

## DTO: Data Transfer Object
- Lost enkele problemen op:
	- Overposting
	- Overfetching
	- Updating Domain klassen en om geen clients stuk te maken
- Karakteristieken:
	- Bevat geen business logica
	- Bevat enkel data
	- Kan gedeeld worden met (C#) clients

```cs
public static class PizzaDto{

public class Index {

	public int Id { get; set; }

	public string Name { get; set; }

	public decimal Price { get; set; }

}
public class Detail {
	public int Id { get; set; }

	public string Name { get; set; }

	public decimal Price { get; set; }

	public List<IngredientDto.Index> Ingredients { get; set; }
}

public class Create {
	public string Name { get; set; }

	public decimal Price { get; set; }
}
public class Edit : Create { // Caution with Inheritance

	public int Id { get; set; }

}}
```

**DTO**: Bevindt zich in de "/Shared" folder. 
**Domein**: Meestal in de /Models folders of in een apart domein project.

### Validator
> a.d.h.v. FluentValidation.

```cs
public class CustomerCreateDtoValidator
: AbstractValidator<CustomerCreateDto>
{
public CustomerCreateDtoValidator() // Constructor
{
	RuleFor(c => c.FirstName).NotEmpty();
	RuleFor(c => c.LastName).NotEmpty().MaximumLength(150);
	RuleFor(c => c.Discount).GreaterThan(0).LessThan(1);
}}
```

```cs
public class CustomerCreateDto {

	public string LastName { get; set; }

	public string FirstName { get; set; }

	public decimal Discount { get; set; }

public class Validator : AbstractValidator<CustomerCreateDto> {

	public Validator()
{
	RuleFor(c => c.FirstName).NotEmpty();
	RuleFor(c => c.LastName).NotEmpty().MaximumLength(150);
	RuleFor(c => c.Discount).GreaterThan(0).LessThan(1);
}}}
```


### Middleware
Iets dat getriggerd wordt voor of na een request.

Vb van mogelijke middleware:
```cs
[HttpPost]

public IActionResult Create(PizzaDto.Create dto)

{

Pizza pizza = new()

{

Name = dto.Name,

IsGlutenFree = dto.IsGlutenFree

};

PizzaService.Add(pizza);

return CreatedAtAction(nameof(Create), new { id = pizza.Id });

}
```

In `program.cs` wordt deze middleware effectief opgeroepen:
```cs
builder.Services
.AddValidatorsFromAssemblyContaining<PizzaDto.Create.Validator>()
.AddFluentValidationAutoValidation();
```

`program.cs`is waar we de Dependency Injection (DI) container opzetten.
-> `builder.Services.AddFluentValidationRulesToSwagger();`

## In het kort
- Documentatie is belangrijk wanneer je een web API deelt.
- Gebruik geen domein objecten als DTO's!
- Valideer de inkomende requests ten minste op de server side!
----
## Images
Bewaar geen images in de databank.
Bewaar ze ergens waar ze gebackupd kunnen worden.

Binary Large Object (BLOB) storage is meestal een gepastere manier om foto's te bewaren.


## Filter 

```cs
// Index component
[Parameter, SupplyParemeterFromQuery]
public string? Searchterm {get; set;}
```

Om zaken uit de url te halen. Enkel componenten met een "/" pad kunnen gebruik maken van de `SupplyParameterFromQuery`. Dit maakt het bv. onmogelijk bruikbaar in de `ProductFilters` component, dus we moeten de `Searchterm` doorgeven vanuit de index




```cs
// Index.razor.cs
protected override async Task OnParametersSetAsync()

{
	ProductRequest.Index request = new()
	{
		Searchterm = Searchterm,
	};

var response = await ProductService.GetIndexAsync(request);

products = response.Products;

}
```

```cs
// Client/Products/ProductService.cs
public async Task<ProductResult.Index>

GetIndexAsync(ProductRequest.Index request)

{
	var response = await client.GetFromJsonAsync
	<ProductResult.Index>
	($"{endpoint}?searchterm={request.Searchterm}");
	return response!;
}

```
`SearchTerm` gebruiken in `GetIndexAsync`

```cs
// ProductFilters.razor.cs
[Parameter, EditorRequired] // EditorRequired zal een melding tonen indien er geen parameter meegegeven werd.
public string? Searchterm {get;set;} = default;
```

```cs
// Client/Products/Index.razor
<ProductFilters Searchterm = "@Searchterm" />
```

```cs
// ProductFilters.razor
<input class="input" type="search" placeholder="Zoeken..."
value="@searchTerm" @onchange="SearchTermChanged">

```

```cs
// ProductFilters.razor.cs

[Parameter, EditorRequired]

public string? Searchterm { get; set; } = default!;

private string? searchTerm;

protected override void OnParametersSet()

{

//Set the field equal to the parameter.

searchTerm = Searchterm;

}

private void SearchTermChanged(ChangeEventArgs args)

{

// When the inputfield changes...

searchTerm = args.Value?.ToString();

FilterProducts();

}

private void FilterProducts()

{ // Navigate to the current page with the new SearchTerm parameter.

Dictionary<string, object?> parameters = new();

parameters.Add(nameof(searchTerm), searchTerm);

var uri = NavigationManager.GetUriWithQueryParameters(parameters);

NavigationManager.NavigateTo(uri);

}```


- [Shopping cart](https://hogent-web.github.io/csharp/chapters/08/slides/index.html#46)

---
# H9
Dapper => ORM

```cs
// DbContext
public class BogusDbContext : DbContext
{
	public DbSet<Product> Products => Set<Product>(); // Representeert een table in de database.

	public BogusDbContext(DbContextOptions<BogusDbContext> options)
	: base(options) {} 

	protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
	{
	base.OnConfiguring(optionsBuilder);
	optionsBuilder.EnableDetailedErrors();
	optionsBuilder.EnableSensitiveDataLogging();


	// optionsBuilder.UseInMemoryDatabase(databaseName: "BogusDb"); // Optioneel als in memory db nodig is.

	modelBuilder.ApplyConfigurationsFromAssembly(typeof(BogusDbContext).Assembly) // Elke keer toevoegen als we nieuwe configs apart toevoegen! Zie wat lager onder configuration grouping.

	}

	protected override void OnModelCreating(ModelBuilder modelBuilder)
	{
	modelBuilder.Entity<Product>()
	.Property(x => x.Name)
	.HasMaxLength(50)
	.IsRequired();
	}
}

```

DbContext klasse is een noodzakelijk onderdeel van het Entity Framework.
Een instantie van DbContext komt overeen met een sessie met de database.


## Entity Base class
Elke entiteit in het domein zou moeten afstammen van deze klasse.
bv:
```cs
public abstract class Entity
{
	public int Id { get; protected set; }
	public DateTime CreatedAt { get; set; }
	public DateTime UpdatedAt { get; set; }
// other stuff
}
```

```cs
public class Product : Entity
{/*Implementation here */
private Product(){} // Best altijd zelf eentje meegeven om issues te voorkomen.
}
```

 Extra configuratie kan worden toegevoegd of overschreven in de OnModelCreating-methode van de afgeleide context met behulp van de krachtige ModelBuilder API. Configuratie met de Fluent API heeft de hoogste prioriteit en zal conventies en gegevensannotaties overschrijven zonder de entity-klassen te wijzigen.


## Configuration grouping
OnModelCreating config overzichtelijk houden dus afzonderen.

```cs
class ProductConfiguration : IEntityTypeConfiguration<Product>
{
	public void Configure(EntityTypeBuilder<Product> builder)
	{
		builder.Property(x => x.Name)
		.HasMaxLength(50);
		.IsRequired();
		
		builder.OwnsOne(x => x.Price).Property(x => x.Value);
	}
}
```

## Lifetime
Meestal vrij korte levensduur van een DbContext instantie.
```cs
// Server/Program.cs
builder.Services.AddDbContext<BogusDbContext>();
```

## [Triggers](https://hogent-web.github.io/csharp/chapters/09/slides/index.html#27)
![[Cs_Triggers.png]]


## Effectieve db gebruiken (sqlserver)
```cs
// Server/Program.cs
builder.Services.AddDbContext<BogusDbContext>(options =>{
	options.UseSqlServer
	(
		builder.Configuration.GetconnectionString("SqlServer")
	)
})
```

```
{

	"ConnectionStrings": {

		"Storage": "YOUR_BLOB_STORAGE_CONNECTION_STRING_HERE",

		"SqlServer": "Server=localhost,1433;Database=Csharp.BogusDb;User=sa;Password=p@ssw0rd"

}

}
```


## Overriding default conventions

```cs
// BogusDbContext.cs
protected override void ConfigureConventions(ModelConfigurationBuilder configBuilder)
{
// All decimals should have 2 digits after te comma
configBuilder.Properties<decimal>().HavePrecision(18 /* Precision */, 2 /* Scale */);
// Max Length of NVARCHAR that can be indexed
configBuilder.Properties<string>().HaveMaxLength(4_000);
}


// Other methods omitted

protected override void ConfigureConventions(ModelConfigurationBuilder configurationBuilder)

{

// All decimals should have 2 digits after the comma

configurationBuilder.Properties<decimal>().HavePrecision(18, 2);

// Max Length of a NVARCHAR that can be indexed

configurationBuilder.Properties<string>().HaveMaxLength(4_000);

}
```

- Precision: Het totale aantal nummers dat toegelaten zijn in het nummer. De lengte als het ware. bv. 3; dan is het grootste nummer 999. (Scale 0)
- Scale: Het aantal nummers van de precision value die achter de komma vallen. Verder gaande op ons voorbeeld, als we bv. 2 nemen; dan is het grootste nummer nog maar 9,99.

## Triggered package output 
```cs
// Sever/AppSettings.json
{
	"ConnectionStrings": {
		"Storage": "YOUR_CONNECTION_STRING_HERE",
		"SqlServer": "YOUR_CONNECTION_STRING_HERE"
},
	"Logging": {
		"LogLevel": {
			"Default": "Information",
			"Microsoft.AspNetCore": "Warning",
			"EntityFrameworkCore.Triggered" : "Warning"
		}
	},
	"AllowedHosts": "*"
}
```


## Default values for entities

```cs
// Persistence/Configurations/Entityconfiguration.cs

class EntityConfiguration<T> : IEntityTypeConfiguration<T> where T : Entity
{
	public virtual void Configure(EntityTypeBuilder<T> builder)
	{
		// All tables are singular named and have the name of the Entity
		builder.ToTable(typeof(T).Name);
		// All entities can be soft deleted but are not by default
		builder.Property(x => x.IsEnabled).IsRequired().HasDefaultValue(true).ValuegeneratedNever();

		// Default SQL constraint for CreatedAt and UpdatedAt
		builder.Property(x => x.CreatedAt).HasDefaulktValueSql("GETUTCDATE()");
		builder.Property(x => x.UpdatedAt).HasDefaultValueSql("GETUTCDATE()").IsConcurrencyToken();
	}
}
```

- IsConcurrencyToken() : Configures whether this property should be used as a concurrency token. When a property is configured as a concurrency token the value in the database will be checked when an instance of this entity type is updated or deleted during [SaveChanges()](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.dbcontext.savechanges?view=efcore-8.0#microsoft-entityframeworkcore-dbcontext-savechanges) to ensure it has not changed since the instance was retrieved from the database. If it has changed, an exception will be thrown and the changes will not be applied to the database.

![[Cs_Configurations.png]]
- Voor elke EntityConfiguration klasse moet dit aangepast worden indien we gebruik maken van een eigen EntityConfiguration klasse voor deze entiteit.

### Column name aanpassen (change column name)
Mogelijk door aan de gewenste entiteit de configuration klasse het volgende toe te voegen aan de builder:
```cs
// Persistence/Configurations/ProductConfiguration.cs
internal class ProductConfiguration : EntityConfiguration<Product>
{
	public override void Configure(EntityTypeBuilder<Product> builder)
	{
	base.Configure(builder);
	builder.OwnsOne(x => x.Price)
	.Property(x => x.Value)
	.HasColumnName(nameof(Product.Price)); // Deze lijn is hiervoor nodig.
	}
}
```

#### OwnsOne / OwnsMany VS HasOne/HasMany
OwnsOne/-Many mag enkel gebruikt worden voor ValueObjects om het object op te slaan bij de Entiteit waartoe het behoort.
![[Cs_OwnsVsHas.png]]

### Ervoor zorgen dat alles mapped is.

- Properties met {get;} worden niet automatisch gemapped! Hiervoor dienen de .Property(x => x.Value). 
	- Indien we private set zouden gebruiken, zou het wel gemapped worden, maar indien het niet nodig is, wordt dit niet aangeraden.

```cs
// Persistence/Configurations/XXX-Configuration.cs
internal classs OrderLineConfiguration : EntityConfiguration<OrderLine>{
	public override void Configure(EntityTypeBuilder<OrderLine> builder)
	{
		base.Configure(builder);
		// Door {get;} niet mapped.
		builder.Property(x => x.Quantity);
		builder.Property(x => x.Description);
		
		// Value Object mapping en hernoemen van kolom
		builder.OwnsOne(x => x.Price) // OwnsOne, dus prijs behoort tot Entiteit.
		.Property(x=> x.Value) // Niet mapped door de {get;}
		.HasColumnName(nameof(OrderLine.Price));
		// 1 to many relatie met een cascade beperking
		builder.HasOne(x => x.Product).WithMany()
		.OnDelete(DeleteBehavior.Restrict)
	}
}

```


### Tracking vs. No-tracking
Tracking is de standaard manier. EF Core zal info bewaren over een entiteit instantie en de veranderingen zullen doorgevoerd worden tijdens de `SaveChanges();`

No-tracking is handig bij readonly scenario's. Ze zijn namelijk sneller om uit te voeren. 

```cs
// Tracking, default.
var blog = context.Blogs.SingleOrDefault(b => b.BlogId == 1);
blog.Rating = 5;
context.SaveChanges();
```

```cs
// No tracking
var blogs = context.Blogs.AsNoTracking().ToList();
```

### Loading (related) data
- **Eager Loading**
	- Meest gebruikte manier. Data wordt deel van de query zelf.
	- `Include()` Data wordt in het query resultaat geplaatst. (Denk aan Join in SQL)
	- Soms is het ook interessant om te filteren op welke data opgehaald dient te worden.
	```cs
	using (var context = new BloggingContext()){
		var blogs = context.Blogs
		.Include(blog => blog.Posts)
	//	.Include(blog => blog.Owner.Where(a => a.x < 10)) // Voeg toe welke nodig zijn. Filteren is ook een optie. 
		.ToList();
	}
	```
	- Multi-level includes kunnen ook m.b.v. `ThenInclude()`
	```cs
	var blogs = context.Blogs
	.Include(blog => blog.Posts)
	.ThenInclude(post => post.Author)
	.ThenInclude(author => author.Photo)
	.ToList();
```
- Explicit Loading (niet te kennen)
	- Data wordt expliciet op een later tijdstip geladen.
	- Zelden gebruikt.
- Lazy Loading (niet te kennen)
	- Data wordt transparant geladen terwijl het nodig is.
	- Kan overbodige "roundtrips" naar de db veroorzaken, hiervoor dienen voorzorgsmaatregelen genomen te worden.

### Saving Data
#### Item toevoegen (Adding an item)
`DbSet.Add(DbObj)`: Om een item toe te voegen aan de db. Deze moet gepersisteerd worden d.m.v. `context.SaveChanges();`
```cs
using (var context = new BloggingContext())
{
	var blog = new Blog { Url = "http://example.com" };
	context.Blogs.Add(blog);
	context.SaveChanges();
}
```

#### Update 
Hier dienen we eerst het gewenste item op te halen uit de db. Dan voeren we de aanpassing erop toe en tot slot persisteren we het d.m.v. `context.SaveChanges();`

```cs
using (var context = new BloggingContext())
{
	var blog = context.Blogs.First();
	blog.Url = "http://example.com/blog";
	context.SaveChanges();
}
```

#### Verwijderen (delete)
Ook hier dienen we het item eerst op te halen.
We kunnen het vervolgens verwijderen d.m.v. `context.DbSet.Remove(dbItem);` op te roepen, vervolgd door `context.SaveChanges();` om  het verwijderen door te voeren.

```cs
using (var context = new BloggingContext())
{
	var blog = context.Blogs.First();
	context.Blogs.Remove(blog);
	context.SaveChanges();
}
```

#### Meerdere veranderingen tegelijkertijd. (multiple operations)
We kunnen alles binnen het using(context) block eigenlijk zien als een transactie. Hierbinnen worden alle gewenste veranderingen aangegeven en vervolgens worden ze doorgevoerd met de `SaveChanges()` methode.

```cs

using (var context = new BloggingContext())
{
	// add
		context.Blogs.Add(new Blog { Url = "http://example.com/blog_one" });
		context.Blogs.Add(new Blog { Url = "http://example.com/blog_two" });
	var firstBlog = context.Blogs.First();
	firstBlog.Url = ""; // update
	var lastBlog = context.Blogs.OrderBy(e => e.BlogId).Last();
	context.Blogs.Remove(lastBlog); //delete
	context.SaveChanges();
}
```


```cs
using (var context = new BloggingContext())
{
	var blog = new Blog
	{
		Url = "http://blogs.msdn.com/dotnet",
		Posts = new List<Post>
		{
			new Post { Title = "Intro to C#" },
			new Post { Title = "Intro to VB.NET" },
			new Post { Title = "Intro to F#" }
		}
	};
	context.Blogs.Add(blog);
	context.SaveChanges();
}
```

### Dapper VS EFC
#### Dapper
- Eigen queries schrijven
- Goed voor kleine projecten.

#### Entity Framework Core
- Schrijft zelf queries
- Goed voor grote projecten met veel tables.
---
## H10 - Authentication
JWT > Cookies: Alles is toch server-side rendered.

### Iets afzonderen voor een bepaalde rol
#### Pagina zelf
- Bv. `AddWeather.razor` pagina:
	Dit doen we met behulp van: 
	`@attribute [Authorize(Roles = "Administrator")]`
	te plaatsen bovenaan in de file, onder `@page ""`, `@using WeatherStation.Shared` en de `@Inject`'s. 

#### In de navigatie
In de navigatie of elders kunnen we ook zaken afzonderen m.b.v. `<AuthorizeView Roles= "Role"> </AuthorizeView>`

```html
<AuthorizeView Roles="Administrator">
	<div class="nav-item px-3">
	<NavLink class="nav-link" href="add-weather">
		<span class="oi oi-list-rich" aria-hidden="true">
		</span> Add Weather
	</NavLink>
	</div>
</AuthorizeView>

```

#### Backend - server/api
In de `WeatherForecastController.cs` kunnen we bv. zetten dat enkel administrators een nieuwe weersvoorspelling mogen toevoegen. Dit m.b.v. het `Authorize` attribuut op de `HttpPost`.

```cs
using Microsoft.AspNetCore.Authorization;
using Microsoft.AspNetCore.Mvc;
using WeatherStation.Shared;

namespace WeatherStation.Server.Controllers;

[ApiController]
[Route("[controller]")]
[Authorize] // 👈 Zorgt ervoor dat we aangemeld moeten zijn om hier toegang tot te hebben. Rol is dus hier niet van belang.
public class WeatherForecastController : ControllerBase
{
    private static readonly string[] Summaries = new[]
    {
        "Freezing", "Bracing", "Chilly", "Cool", "Mild", "Warm", "Balmy", "Hot", "Sweltering", "Scorching"
    };

    private static readonly List<WeatherForecast> forecasts = new();

    static WeatherForecastController()
    {
        forecasts.AddRange(Enumerable.Range(1, 5).Select(index => new WeatherForecast
        {
            Date = DateTime.Now.AddDays(index),
            TemperatureC = Random.Shared.Next(-20, 55),
            Summary = Summaries[Random.Shared.Next(Summaries.Length)]
        }));
    }

    [HttpGet]
    public IEnumerable<WeatherForecast> GetForecasts()
    {
        return forecasts;
    }

    [HttpPost]
    [Authorize(Roles = "Administrator")] // 👈 ADMIN ONLY MAKEN.
    public WeatherForecast CreateForecast(WeatherForecast forecast)
    {
        forecasts.Add(forecast);
        return forecast;
    }
}
```

---
## H11 - Playwright testing
Gelijkaardig aan [Cypress](https://www.cypress.io/). (Elke browser, elk platform, 1 API)
### Managed vs Unmanaged
- **Managed dependencies**: Zaken die enkel door je applicatie toegankelijk zijn; interacties die niet extern zichtbaar zijn. Bv. Applicatie DB. Zelf hier verantwoordelijk voor.
- **Unmanaged dependencies**: Zaken die extern zijn en waar je gebruik van maakt in je applicatie. Deze moet je 'mocken', code van externe partijen (Azure BLOB e.g.) dien je niet te testen. Echter wel of het binnen je applicatie werkt hoe je verwacht.

### Levels of testing 
> In het kort, playwright gaat voor het laatste om alles tegelijkertijd te testen.

- Domein: Unit tests
- Service: Unit en integration tests
	- Test de request-response pipeline niet!
- Persistence layer: Overbodig hier.
- Server: Unit en integration tests
	- Endpoints kunnen getest worden in de controllers en ook de service en domein laag kunnen allemaal tegelijkertijd getest worden.
- Client: Unit en integration tests. (bv. a.d.h.v. [bUnit](https://bunit.dev/))
- Alles tegelijkertijd testen: Mogelijk, maar duurt langer. Kan meer vertrouwen in app geven.

### Testing
We testen of het klikken op een counter knop effectief de counter verhoogd.
```cs
[Parallelizable(ParallelScope.Self)]
public class CounterTests : PageTest

{
	private const string ServerBaseUrl = "https://localhost:5001";

	[Test]
	public async Task Clicking_Counter_Updates_Count()
	{
		// Navigate to the counter page
		await Page.GotoAsync($"{ServerBaseUrl}/counter");
		
		// Wait until the counter page is really there.
		await Page.WaitForSelectorAsync("h1");
		
		// Click on counter
		await Page.ClickAsync("text=Click Me");
		
		// Assert
		var content = await Page.TextContentAsync("p");
		Assert.AreEqual("Current count: 1", content);
	}

}
```

Let op: 
```cs
// Click on counter
await Page.ClickAsync("text=Click Me");
```

Beter om het te vervangen door:
```html
<!-- In het HTML element -->
<button data-test-id="counter-button" class="btn btn-primary"
@onclick="IncrementCount">Click me</button>
```

```cs 
await Page.ClickAsync("data-test-id=counter-button");
```

---
# Commands
> Niet nodig voor examen dus ook niet verder aangevuld geweest sinds ik het door had. Wellicht compleet genoeg indien nood aan, basis staat er in. :)

Initialise a git repo:
```
git init
dotnet new gitignore
```

Build the application:
```
dotnet build
```

Run the application:
```
dotnet run
```

Create a new console application:
```
dotnet new console -o App -f net6.0 --use-program-main
```
- -o to specify the name: App

Create a Class Library
```
dotnet new classlib -o Domain -f net6.0
```

Link the Domain Class Library to the application (from **src** folder.)
```
dotnet add App/App.csproj reference Domain/Domain.csproj
```

Create a new solution:
```
dotnet new sln
```

Add projects to .sln
```
cd .. // We must be in the correct directory.

dotnet sln add src/app/App.csproj
dotnet sln add src/domain/Domain.csproj
```

Create a new xUnit Test Project called Domain.Tests (in tests folder)
```
dotnet new xunit -n Domain.Tests -f net6.0
```

Add a reference to the Domain project
```
dotnet add .\Domain.Tests\Domain.Tests.csproj reference ..\src\Domain\Domain.csproj
```

Playwright commands
![[Cs_Playwright_commands.png]]![[Cs_Playwright_Commands_2.png]]

Run serverproj. app: `dotnet run`
Run tests (from test folder): `dotnet test`
