## Description

This documentation will show you how to run a laravel project quickly.

---

Welcome to follow `LaravelTips` on wechat, this account will focus on the services to serve the laravel developers, we try to help those developers to learning the laravel framework better and faster.

![](http://ww4.sinaimg.cn/large/76dc7f1bjw1f23moqj4qzj20by0bywfa.jpg)

## Installation

We are using [homestead]() as our local development environment, and before we get started, make sure you already install `homestead` and `vagrant` in your local machine.

### 1. Download the source code

    git clone {project_url}

### 2. Setup homestead

Open `Homestead.yaml` by this command:

    homestead edit

Modify it like this:

    folders:
        - map: /Users/.../demo-name {your laravel project path}
          to: /home/vagrant/demo-name

    sites:
        - map: demo-name.app
          to: /home/vagrant/demo-name/public

    databases:
        - demo-name

Restart homestead:

    homestead provision

### 3. Install package

    composer install

### 4. Generate `.env` file

Copy `.env.example` to `.env`

```
cp .env.example .env
```

### 5. Modify `hosts` file

Open it by this command:

	sudo vi /etc/hosts

Add this line to file:

	127.0.0.1  	demo-name

Finally, you can access http://demo-name.app to check the result.
