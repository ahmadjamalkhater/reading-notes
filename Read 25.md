## Basics of Claims

When dealing with claims-based authorization, it's essential to understand what claims are. A claim is a name-value pair that represents a specific piece of information about a user. For instance, a claim might include information like a user's date of birth, role, or membership status. Claims provide a way to make authorization decisions based on user attributes rather than just roles.

## How Claims-Based Authorization Works

In claims-based authorization, an identity is created for a user, and this identity is associated with one or more claims. These claims are issued by a trusted party, and they represent specific attributes of the user. When accessing a resource, the system checks the claims associated with the user's identity to determine if they have the necessary attributes to access that resource.

For example, consider a scenario where a night club allows access based on the user's age. The doorman checks the "DateOfBirth" claim associated with the user's identity and decides whether to grant access based on their age.

## Implementation in ASP.NET Core

In ASP.NET Core, you can implement claims-based authorization using policies. A policy is a set of requirements that must be fulfilled for a user to access a particular resource. Policies are declarative and can be applied to controllers, actions, or Razor Pages.

To implement claims-based authorization, you can follow these steps:

1. Define and register a policy specifying the required claim(s) for access.
2. Apply the `[Authorize]` attribute with the policy name to the controller or action.

Here's an example of how to define a policy and apply it:

```csharp
services.AddAuthorization(options =>
{
    options.AddPolicy("EmployeeOnly", policy => policy.RequireClaim("EmployeeNumber"));
});

[Authorize(Policy = "EmployeeOnly")]
public IActionResult VacationBalance()
{
    return View();
}