# 🧾 Frappe / ERPNext Bench Commands – Complete Cheat Sheet
---

# 🚀 Setup & Basics

## Create a New Site

```bash
bench new-site mysite.local
```

## Start Development Server

```bash
bench start
```

## Stop Server

```bash
Ctrl + C
# OR
bench stop
```

---

# 📦 App Management

## Create a New App

```bash
bench new-app my_app
```

## Get App from GitHub

```bash
bench get-app app_name
```

## Get ERPNext App

```bash
bench get-app erpnext --branch version-15
```

## Install App in Site

```bash
bench --site mysite.local install-app my_app
```

## Install ERPNext in Site

```bash
bench --site mysite.local install-app erpnext
```

---

# 🔧 Site Management

## List Sites

```bash
bench site list
```

## Open Site Console

```bash
bench --site mysite.local console
```

## Run Python Command in Site Context

```bash
bench --site mysite.local execute app.module.method
```

Example:

```bash
bench --site mysite.local execute frappe.utils.now
```

---

# 🛠️ Maintenance Mode

## Enable Maintenance Mode

```bash
bench --site mysite.local set-maintenance-mode on
```

## Disable Maintenance Mode

```bash
bench --site mysite.local set-maintenance-mode off
```

---

# 🏗️ Build & Assets

## Build Assets

```bash
bench build
```

## Production Build

```bash
bench build --production
```

---

# 🔄 Migration & Updates

## Migrate Site

```bash
bench --site mysite.local migrate
```

## Update Bench (Apps + DB + Build)

```bash
bench update
```

## Restart Bench

```bash
bench restart
```

---

# 🧹 Cache & Cleanup

## Clear Cache

```bash
bench --site mysite.local clear-cache
```

## Clear Website Cache

```bash
bench --site mysite.local clear-website-cache
```

---

# ⚙️ Developer Mode

## Enable Developer Mode

```bash
bench --site mysite.local set-config developer_mode 1
```

## Disable Developer Mode

```bash
bench --site mysite.local set-config developer_mode 0
```

---

# 💻 Bench Console

## Open Bench Console

```bash
bench console
```

---

# 🧪 Debugging & Logs

## View Logs

```bash
bench logs
```

## Watch Logs Live

```bash
bench logs --follow
```

---

# 📁 Database & Backup

## Backup Site

```bash
bench --site mysite.local backup
```

## Restore Site

```bash
bench --site mysite.local restore path/to/backup.sql.gz
```

---

# 🌐 Production Commands

## Setup Production

```bash
sudo bench setup production frappe
```

## Setup NGINX

```bash
bench setup nginx
```

## Setup Supervisor

```bash
bench setup supervisor
```

---

# 🧠 Full Quick Workflow

```bash
bench new-app my_app
bench new-site mysite.local
bench get-app erpnext --branch version-15
bench --site mysite.local install-app erpnext
bench --site mysite.local install-app my_app
bench build
bench start
```

---

# 📌 Tips

* Always run `bench migrate` after installing apps
* Use maintenance mode during updates
* Run `bench build` after frontend changes
* Enable developer mode for custom development

---
