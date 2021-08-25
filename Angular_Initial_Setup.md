### Configuración inicial de Angular

```
ng new frontend
cd frontend
ng serve
estructura
app.component.html
Crear componentes
```

## Creación de componentes
NgModule es el core de angular
ng generate component
ng g c home/header
ng g c home/login
ng g c home/register
ng g c home/footer

ng g c board/list-task
ng g c board/save-task

ng g c admin/list-user
ng g c admin/register-user
ng g c admin/update-user
ng g c admin/register-role
ng g c admin/list-role
ng g c admin/update-role

## Creación de services
# Services
Angular generate service
ng g s services/user servicio que se va a comunicar con el backend user
ng g s services/board servicio que se va a comunicar con el backend board
ng g s services/role servicio que se va a comunicar con el backend role
ng g s services/token-interceptor

Importamos services, cuando son componentes se ponen en las declaraciones. Cuando son servicios se ponen en los Providers de app.module.ts

# Guard
ng g guard guard/auth
proteger ciertas rutas. Se selecciona CanActivate incluye todas las opciones. Es un servicio de protección


# Configuración de rutas (routes)
app-routing.module.ts
cuando el path está en blanco, es lo primero que se visualizará al abrir la aplicación:

```
const routes: Routes = [
  {
    path: '',
    component: LoginComponent,
    pathMatch: 'full'
  },
  {
    path: 'listTask',
    component: ListTaskComponent
  },
  {
    path: 'saveTask',
    component: SaveTaskComponent
  },
  {
    path: 'login',
    component: LoginComponent
  },
  {
    path: 'signUp',
    component: RegisterComponent
  },
  {
    path: 'listUser',
    component: ListUserComponent
  },
  {
    path: 'registerUser',
    component: RegisterUserComponent
  },
  {
    path: 'updateUser',
    component: UpdateUserComponent
  },
  {
    path: 'registerRole',
    component: RegisterRoleComponent
  },
  {
    path: 'listRole',
    component: ListRoleComponent
  },
  {
    path: 'updateRole',
    component: UpdateRoleComponent
  }    
];	
```
pathMatch: es que el path debe ingresarse completo.
