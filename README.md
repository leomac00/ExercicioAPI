﻿# Exercicio API - Book listing API

An API that allows users to control their favorite books.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- .Net Core → Version: 3.1.412;

### Installing

1. Clone the repository to you machine;

2. Create the MySql Schema using the information below:

> server=localhost;port=3306;database=bookapi;uid=root;password=root

3. Run the following commands:

```

dotnet restore

```

```

dotnet ef database update

```

```

dotnet watch run

```

Then just access : https://localhost:5001/swagger/index.html to get information regarding the APIs methods.

### Running

To be able to access all methods you will need to [Register](https://localhost:5001/api/v1/users/register) and then [Log in](https://localhost:5001/api/v1/users/login).

In order to do so you will no to make a POST request to [Register](https://localhost:5001/api/v1/users/register) using the BODY example as described bellow:

```

{

"Name":"AnyName",

"Email":"AnyEmail",

"Password":"AnyPassword"

}

```

After that make another POST request but now to [Log in](https://localhost:5001/api/v1/users/login) using the following BODY example:

```

{

"Email":"AnyEmail",

"Password":"AnyPassword"

}

```

The POST to Login will return a token, this token needs to be used in the Authorization part of the request in order to access the correct user and validate the current session; it will expire after one hour.

## Built With

- [.Net Core](https://dotnet.microsoft.com/download) → Version: 3.1.412;

- [Microsoft.EntityFrameworkCore.Design](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.Design/3.1.17) → Version: 3.1.17;

- [Microsoft.IdentityModel.Tokens](https://www.nuget.org/packages/Microsoft.IdentityModel.Tokens/6.7.1) → Version: 6.7.1;

- [Microsoft.OpenApi](https://www.nuget.org/packages/Microsoft.OpenApi/1.2.3) → Version: 1.2.3;

- [Pomelo.EntityFrameworkCore.MySql](https://www.nuget.org/packages/Pomelo.EntityFrameworkCore.MySql/3.1.2) → Version: 3.1.2;

- [Swashbuckle.AspNetCore](https://www.nuget.org/packages/Swashbuckle.AspNetCore/6.1.5) → Version: 6.1.5;

- [System.IdentityModel.Tokens.Jwt](https://www.nuget.org/packages/System.IdentityModel.Tokens.Jwt/6.7.1) → Version: 6.7.1;

- [Microsoft.AspNetCore.Authentication.JwtBearer](https://www.nuget.org/packages/Microsoft.AspNetCore.Authentication.JwtBearer/3.1.18) → Version: 3.1.18;

- [BCrypt.Net-Core](https://www.nuget.org/packages/BCrypt.Net-Core/1.6.0) → Version: 1.6.0;

## Documentation

In this project all documentation needed was generated using [SWAGGER](https://swagger.io/).

Access [BookAPI/Swagger](https://localhost:5001/swagger/index.html) to read the documentation.

Swagger:

![SWAGGER](https://i.imgur.com/eZjol7D.gif)

Examples:

![Examples](https://i.imgur.com/FgDZ36A.gif)

## Authors

- **Leonardo Machado** - _Initial work_ - [LeoMac00](https://github.com/leomac00)
