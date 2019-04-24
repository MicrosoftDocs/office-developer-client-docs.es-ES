---
title: Probar las funciones, la autenticación y la configuración
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: En este tema se describen las pruebas para obtener capacidades y escenarios relacionados con la configuración de una cuenta y la autenticación de un usuario para una red social.
ms.openlocfilehash: 218d5c564dd18e1e72820e31079011e6bb81a33c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329172"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Probar las funciones, la autenticación y la configuración

En este tema se describen las pruebas para obtener capacidades y escenarios relacionados con la configuración de una cuenta y la autenticación de un usuario para una red social.
  
## <a name="getting-capabilities"></a>Obtener capacidades

Un proveedor de Outlook Social Connector (OSC) implementa [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md)y el OSC llama a **GetCapabilities** para obtener la funcionalidad admitida por el proveedor. Las funcionalidades que admite su proveedor para su red social deben conocerse en el punto de la implementación y no deben depender de una llamada a la red social en tiempo real. Por ejemplo, los usuarios de Outlook pueden iniciar Outlook sin conexión y **GetCapabilities** no pueden confiar en la conectividad de red en el momento en que se inicia Outlook. 
  
Al probar el proveedor, debe comprobar que el parámetro __ de cadena Results devuelto por **GetCapabilities** se ajusta al elemento **Capabilities** tal como lo define el esquema XML del proveedor OSC. Para obtener más información, vea [funciones de los elementos XML](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>Configuración de una cuenta

Cuando el OSC configura una cuenta, debe comprobar si se muestra el icono y el nombre de la red social, y si los hipervínculos crear cuenta y olvidar-contraseña aparecen en el cuadro de diálogo Configuración de la cuenta según especifique el proveedor.
  
### <a name="social-network-icon-and-name"></a>Icono y nombre de la red social

Después de obtener la funcionalidad, el OSC puede continuar para obtener el icono y el nombre de la red social llamando a [ISocialProvider:: SocialNetworkIcon](isocialprovider-socialnetworkicon.md) y [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md). Realice las siguientes pruebas para comprobar que estas llamadas a métodos se realizan correctamente.
  
|**Elemento que se va a probar**|**Comportamiento esperado**|
|:-----|:-----|
|Icono de red social  <br/> | El icono de la red social se muestra correctamente en los siguientes lugares del OSC:  <br/>  En el cuadro de diálogo OSC para **cuentas de redes sociales**.  <br/>  En el menú desplegable al intentar agregar una persona como amigo.  <br/>  En el distintivo al seguir a un amigo.  <br/> <br/>**Nota**: puede obtener acceso al cuadro de diálogo para **cuentas de redes sociales** haciendo clic en la pestaña **Ver** en Outlook, en el grupo del **Panel de personas** , en el panel de **personas**y, a continuación, en configuración de la **cuenta**.           |
|Nombre de la red social  <br/> | El nombre de la red social se muestra correctamente en los siguientes lugares del OSC:  <br/>  En el cuadro de diálogo OSC para **cuentas de redes sociales**.  <br/>  En el menú desplegable al intentar agregar una persona como amigo.  <br/>  Como el título del cuadro de diálogo de contraseña cuando se intenta cambiar la contraseña existente.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Mostrar hipervínculos en el cuadro de diálogo de configuración

Después de llamar a **ISocialProvider:: GetCapabilities**, OSC utiliza el valor del elemento **hideHyperlinks** en el parámetro _Results_ para determinar si se debe ocultar o Mostrar la pantalla **haga clic aquí para crear una cuenta** y **olvidar el contraseña?** hipervínculos en el cuadro de diálogo Configuración de la cuenta. Compruebe que si **hideHyperlinks** es **false**, la configuración de la cuenta muestra estas direcciones URL.
  
### <a name="support-to-create-account"></a>Soporte técnico para crear una cuenta

Compruebe que si el __ parámetro Results de la llamada al método **ISocialProvider:: GetCapabilities** tiene el elemento **hideHyperlinks** establecido en **false** y el elemento **createAccountUrl** establecido en **true**, al hacer clic en la dirección URL abre la página en el explorador Web predeterminado.
  
### <a name="support-for-forgotten-password"></a>Compatibilidad con contraseña olvidada

Compruebe que si el __ parámetro Results de la llamada al método **ISocialProvider:: GetCapabilities** tiene el elemento **hideHyperlinks** establecido en **false** y el elemento **forgotPasswordUrl** establecido en **true**, al hacer clic en la dirección URL abre la página en el explorador Web predeterminado.
  
## <a name="authenticating-users"></a>Autenticación de usuarios

Pruebe los siguientes escenarios independientemente de si su proveedor de OSC admite la autenticación básica o la autenticación basada en formularios.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Iniciar sesión por primera vez.  <br/> |El usuario puede iniciar sesión correctamente en la red social.  <br/> |
|Inicio de sesión con una contraseña formada por una variedad de caracteres, incluidos los caracteres Unicode y los signos de puntuación.  <br/> |El usuario puede iniciar sesión correctamente en la red social, independientemente del tipo de caracteres que se usan en la contraseña.  <br/> |
|El cuadro de diálogo para **cuentas de redes sociales** que muestra el nombre de usuario o el identificador.  <br/> |Una vez que el usuario ha iniciado sesión correctamente en la red, el cuadro de diálogo de OSC para **cuentas de red social** muestra el identificador o nombre de usuario que ha iniciado sesión.  <br/> |
|Se produce un error en la autenticación.  <br/> |El OSC muestra el error **nombre de usuario o contraseña no válidos**.  <br/> |
|No se puede conectar a la red social.  <br/> |El OSC muestra que **no se encuentra el servidor**de errores.  <br/> |
|Poder recuperar elementos.  <br/> |Una vez que el usuario se ha autenticado, se debe permitir toda la actividad. No hay errores al obtener los datos o las actividades de los amigos.  <br/> |
|Iniciar sesión en la red social después de reiniciar Outlook.  <br/> |Si el proveedor de OSC permite almacenar en caché la contraseña, después de que el usuario se autentique por primera vez, el usuario no se le pedirá posteriormente ninguna credencial siempre que el OSC intente obtener datos de la red social.  <br/> |
   
Además, si el proveedor de OSC admite la autenticación basada en formularios, pruebe también el siguiente escenario.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|El OSC obtiene una dirección URL a un formulario para que el usuario inicie la sesión mediante la llamada a [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md).  <br/> |El OSC abre la dirección URL en el explorador predeterminado del usuario y la página web permite al usuario especificar credenciales para iniciar sesión en la red social.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de capacidades](capabilities-xml-elements.md)  
- [Autenticación básica](basic-authentication.md) 
- [Autenticación basada en formularios](forms-based-authentication.md)
- [Preparación para la publicación de un proveedor OSC](getting-ready-to-release-an-osc-provider.md)

