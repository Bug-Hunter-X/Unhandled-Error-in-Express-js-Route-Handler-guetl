# Unhandled Error in Express.js Route Handler

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid or unexpected input.  Specifically, this example shows a route that retrieves a user by ID. If an invalid ID is provided, the application may crash or return an unexpected response.

## Bug Description

The `/users/:id` route retrieves a user from an array. If the `id` parameter cannot be parsed as an integer, or if no user with that ID exists, there's no error handling.  This can lead to runtime errors or inconsistent responses.

## Solution

The solution includes comprehensive error handling. It checks if `userId` is a number and handles the case where a user with the given ID is not found, returning appropriate HTTP status codes and messages.