# Cookies

## What are Cookies?

Have you ever noticed that when you visit a website, it **remembers things about you?** like your **username** or items in your **shopping cart?** That's because of **Cookies**.

- Cookies are **small piece of data** that **website store** on your computer or mobile device.

- They are **important in web development** because they allow websites to **remember information about the user**, such as their preferences or **login credentials**.

## How Cookies Works?

When a **user sen a request** to a server, the server treats **each request** as if it's a **new user**.

- To **recognize returning user**, we **add a cookie** to the **response** from the server.

- The **cookie is stored** on user's **browser**, and whenever they **send a new request**, the browser automatically ads the cookie to it.

- This allow the **server to recognize** the **user** and **personalize** their experience.

## Setting Cookies

To **create a cookie** using Javascript, you can use the **document.cookie** property.

```bash
document.cookie = "username = Abhay";
```

You can also add an **expiry date** (in UTC time). and With a **path** parameter, you can also tell the browser what **path the cookie belongs** to.

```bash
document.cookie = "username = Abhay; expires=Thu,4 July 2024 12:00:00 UTC; path=/";
```

## Reading Cookies

To **read** the value of a **cookie** using Javascript, you can use the **document.cookie** property.

```bash
let allCookies = document.cookie;
console.log("All Cookies : " + allCookies);
```
Here you will get all cookies in one string much like, cookie1=value; cookie2=value.

## Deleting Cookies

To delete a cookie using Javascript, you can set **expiration date to past date**, which will cause the browser to remove the cookie from the user's device.

```bash
document.cookie = "username = Abhay; expires=Thu,4 July 2003 12:00:00 UTC";
```

