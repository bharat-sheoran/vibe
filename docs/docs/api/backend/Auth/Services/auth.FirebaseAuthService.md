<<<<<<< HEAD
Defined in: [backend/src/modules/auth/services/FirebaseAuthService.ts:48](https://github.com/saaranshgarg1/vibe/blob/92f3eed6f8b269ad4e4d39a2fa93008a887aa76f/backend/src/modules/auth/services/FirebaseAuthService.ts#L48)
=======
Defined in: [backend/src/modules/auth/services/FirebaseAuthService.ts:48](https://github.com/continuousactivelearning/vibe/blob/2acbe3b478970855555eb5e714d2dc1713e5937b/backend/src/modules/auth/services/FirebaseAuthService.ts#L48)
>>>>>>> 8b14a9cc35ef20bd7bf087ce1213759164e46ae9

Service that implements authentication functionality using Firebase Auth.
Handles user registration, token verification, and password management.

## Implements

## Implements

- [`IAuthService`](../Interfaces/auth.IAuthService.md)

## Constructors

### Constructor

> **new FirebaseAuthService**(`userRepository`): `FirebaseAuthService`

<<<<<<< HEAD
Defined in: [backend/src/modules/auth/services/FirebaseAuthService.ts:60](https://github.com/saaranshgarg1/vibe/blob/92f3eed6f8b269ad4e4d39a2fa93008a887aa76f/backend/src/modules/auth/services/FirebaseAuthService.ts#L60)
=======
Defined in: [backend/src/modules/auth/services/FirebaseAuthService.ts:60](https://github.com/continuousactivelearning/vibe/blob/2acbe3b478970855555eb5e714d2dc1713e5937b/backend/src/modules/auth/services/FirebaseAuthService.ts#L60)
>>>>>>> 8b14a9cc35ef20bd7bf087ce1213759164e46ae9

Creates a new Firebase authentication service instance.
Initializes Firebase Admin SDK with application default credentials.

#### Parameters

##### userRepository

`IUserRepository`

Repository for storing and retrieving user data

#### Returns

`FirebaseAuthService`

## Methods

### changePassword()

> **changePassword**(`body`, `requestUser`): `Promise`\<\{ `message`: `string`; `success`: `boolean`; \}\>

<<<<<<< HEAD
Defined in: [backend/src/modules/auth/services/FirebaseAuthService.ts:150](https://github.com/saaranshgarg1/vibe/blob/92f3eed6f8b269ad4e4d39a2fa93008a887aa76f/backend/src/modules/auth/services/FirebaseAuthService.ts#L150)
=======
Defined in: [backend/src/modules/auth/services/FirebaseAuthService.ts:150](https://github.com/continuousactivelearning/vibe/blob/2acbe3b478970855555eb5e714d2dc1713e5937b/backend/src/modules/auth/services/FirebaseAuthService.ts#L150)
>>>>>>> 8b14a9cc35ef20bd7bf087ce1213759164e46ae9

Changes a user's password in Firebase Auth.
Verifies that passwords match and the user exists before making changes.

#### Parameters

##### body

[`ChangePasswordBody`](../../Other/auth.ChangePasswordBody.md)

Contains the new password and confirmation

##### requestUser

`IUser`

The authenticated user requesting the password change

#### Returns

`Promise`\<\{ `message`: `string`; `success`: `boolean`; \}\>

A promise resolving to a success confirmation object

#### Throws

ChangePasswordError - If passwords don't match or user doesn't exist

#### Implementation of

[`IAuthService`](../Interfaces/auth.IAuthService.md).[`changePassword`](../Interfaces/auth.IAuthService.md#changepassword)

***

### signup()

> **signup**(`body`): `Promise`\<`IUser`\>

<<<<<<< HEAD
Defined in: [backend/src/modules/auth/services/FirebaseAuthService.ts:105](https://github.com/saaranshgarg1/vibe/blob/92f3eed6f8b269ad4e4d39a2fa93008a887aa76f/backend/src/modules/auth/services/FirebaseAuthService.ts#L105)
=======
Defined in: [backend/src/modules/auth/services/FirebaseAuthService.ts:105](https://github.com/continuousactivelearning/vibe/blob/2acbe3b478970855555eb5e714d2dc1713e5937b/backend/src/modules/auth/services/FirebaseAuthService.ts#L105)
>>>>>>> 8b14a9cc35ef20bd7bf087ce1213759164e46ae9

Registers a new user with Firebase Auth and stores user data in the repository.

#### Parameters

##### body

[`SignUpBody`](../../Other/auth.SignUpBody.md)

The validated signup information including email, password, and name

#### Returns

`Promise`\<`IUser`\>

A promise resolving to the newly created user object

#### Throws

Error - If user creation fails in either Firebase or the repository

#### Implementation of

[`IAuthService`](../Interfaces/auth.IAuthService.md).[`signup`](../Interfaces/auth.IAuthService.md#signup)

***

### verifyToken()

> **verifyToken**(`token`): `Promise`\<`IUser`\>

<<<<<<< HEAD
Defined in: [backend/src/modules/auth/services/FirebaseAuthService.ts:76](https://github.com/saaranshgarg1/vibe/blob/92f3eed6f8b269ad4e4d39a2fa93008a887aa76f/backend/src/modules/auth/services/FirebaseAuthService.ts#L76)
=======
Defined in: [backend/src/modules/auth/services/FirebaseAuthService.ts:76](https://github.com/continuousactivelearning/vibe/blob/2acbe3b478970855555eb5e714d2dc1713e5937b/backend/src/modules/auth/services/FirebaseAuthService.ts#L76)
>>>>>>> 8b14a9cc35ef20bd7bf087ce1213759164e46ae9

Verifies a Firebase authentication token and returns the associated user.

#### Parameters

##### token

`string`

The Firebase ID token to verify

#### Returns

`Promise`\<`IUser`\>

A promise that resolves to the user data associated with the token

#### Throws

Error - If the token is invalid or verification fails

#### Implementation of

[`IAuthService`](../Interfaces/auth.IAuthService.md).[`verifyToken`](../Interfaces/auth.IAuthService.md#verifytoken)
