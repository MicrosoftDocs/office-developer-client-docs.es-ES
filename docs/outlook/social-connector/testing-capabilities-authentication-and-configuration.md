---
title: Probar las funciones, la autenticación y la configuración
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: En este tema se describen las pruebas para obtener capacidades y escenarios en torno a la configuración de una cuenta y la autenticación de un usuario para una red social.
ms.openlocfilehash: 218d5c564dd18e1e72820e31079011e6bb81a33c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423506"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Probar las funciones, la autenticación y la configuración

En este tema se describen las pruebas para obtener capacidades y escenarios en torno a la configuración de una cuenta y la autenticación de un usuario para una red social.
  
## <a name="getting-capabilities"></a>Obtención de funcionalidades

Un proveedor de Outlook Social Connector (OSC) implementa [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)y el OSC llama a **GetCapabilities** para obtener la funcionalidad admitida por el proveedor. Las funcionalidades que admite su proveedor para la red social deben conocerse en el punto de implementación y no deben depender de una llamada a la red social en tiempo real. Por ejemplo, los usuarios de Outlook pueden iniciar Outlook sin conexión y **GetCapabilities** no puede confiar en la conectividad de red en el momento en que se inicia Outlook. 
  
Al probar el proveedor, debe  comprobar que el parámetro de cadena de resultados devuelto por **GetCapabilities** se ajusta al elemento **capabilities** tal como lo define el esquema XML del proveedor de OSC. Para obtener más información, vea [Capabilities XML Elements](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>Configuración de una cuenta

Cuando el OSC configura una cuenta, debe comprobar si se muestran el icono y el nombre de la red social, y que los hipervínculos crear cuenta y contraseña olvidada aparecen en el cuadro de diálogo de configuración de la cuenta según lo especificado por el proveedor.
  
### <a name="social-network-icon-and-name"></a>Nombre y icono de red social

Después de obtener las funcionalidades, el OSC puede proceder a obtener el icono y el nombre de la red social llamando a [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) e [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md). Realice las siguientes pruebas para comprobar que estas llamadas de método se realizan correctamente.
  
|**Elemento que se debe probar**|**Comportamiento esperado**|
|:-----|:-----|
|Icono de red social  <br/> | El icono de la red social se muestra correctamente en los siguientes lugares del OSC:  <br/>  En el cuadro de diálogo OSC para cuentas **de red social**.  <br/>  En el menú desplegable cuando intenta agregar a una persona como un amigo.  <br/>  En el distintivo al seguir a un amigo.  <br/> <br/>**NOTA:** Para obtener acceso al cuadro de  diálogo de cuentas de  red **social,** haga clic en la pestaña Ver de Outlook, en el grupo Panel de personas, haga clic en Panel de personas y, a continuación, haga clic en Configuración de **la cuenta.**            |
|Nombre de la red social  <br/> | El nombre de la red social se muestra correctamente en los siguientes lugares del OSC:  <br/>  En el cuadro de diálogo OSC para cuentas **de red social**.  <br/>  En el menú desplegable cuando intenta agregar a una persona como un amigo.  <br/>  Como título del cuadro de diálogo de contraseña al intentar cambiar la contraseña existente.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Mostrar hipervínculos en el cuadro de diálogo de configuración

Después de llamar a **ISocialProvider::GetCapabilities,** el OSC usa el  valor del elemento **hideHyperlinks** en el parámetro de resultados para determinar si desea ocultar o mostrar los hipervínculos Click **here to create an account** and Forgot **your password?** en el cuadro de diálogo de configuración de la cuenta. Compruebe que si **hideHyperlinks** es **false,** la configuración de la cuenta muestra estas direcciones URL.
  
### <a name="support-to-create-account"></a>Soporte técnico para crear una cuenta

Compruebe que  si el parámetro de resultados de la llamada al método **ISocialProvider::GetCapabilities** tiene el elemento **hideHyperlinks** establecido en **false** y el elemento **createAccountUrl** establecido en **true**, al hacer clic en la dirección URL se abre la página en el explorador web predeterminado.
  
### <a name="support-for-forgotten-password"></a>Compatibilidad con contraseña olvidada

Compruebe que  si el parámetro de resultados de la llamada al método **ISocialProvider::GetCapabilities** tiene el elemento **hideHyperlinks** establecido en **false** y el elemento **forgotPasswordUrl** establecido en **true**, al hacer clic en la dirección URL se abre la página en el explorador web predeterminado.
  
## <a name="authenticating-users"></a>Autenticación de usuarios

Pruebe los siguientes escenarios independientemente de si su proveedor de OSC admite la autenticación básica o la autenticación basada en formularios.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Iniciar sesión por primera vez.  <br/> |El usuario puede iniciar sesión correctamente en la red social.  <br/> |
|Iniciar sesión con una contraseña que se conste de una variedad de caracteres, incluidos signos de puntuación y caracteres Unicode.  <br/> |El usuario puede iniciar sesión correctamente en la red social, independientemente del tipo de caracteres usados en la contraseña.  <br/> |
|Cuadro de diálogo de cuentas **de red social** que muestra el nombre de usuario o el identificador.  <br/> |Una vez que el usuario haya iniciado sesión correctamente en la red, el cuadro de diálogo de OSC para cuentas de red **social** muestra el nombre de usuario o el identificador que ha iniciado sesión.  <br/> |
|Se produce un error en la autenticación.  <br/> |El OSC muestra el error Nombre **de usuario o contraseña no válidos.**  <br/> |
|No se puede conectar a la red social.  <br/> |El OSC muestra el error **No se encuentra el servidor**.  <br/> |
|Poder recuperar elementos.  <br/> |Una vez que el usuario se haya autenticado, se debe permitir toda la actividad. No hay errores al obtener datos o actividades de amigos.  <br/> |
|Iniciar sesión en la red social después de reiniciar Outlook.  <br/> |Si el proveedor de OSC permite el almacenamiento en caché de la contraseña, después de que el usuario se haya autenticado por primera vez, no se le pedirán credenciales al usuario cuando el OSC intente obtener datos de la red social.  <br/> |
   
Además, si el proveedor de OSC admite la autenticación basada en formularios, pruebe también el siguiente escenario.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|El OSC que obtiene una dirección URL a un formulario para que el usuario inicie sesión llamando a [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md).  <br/> |El OSC abre la dirección URL en el explorador predeterminado del usuario y la página web permite al usuario escribir credenciales para iniciar sesión en la red social.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Capacidades de elementos XML](capabilities-xml-elements.md)  
- [Autenticación básica](basic-authentication.md) 
- [Autenticación basada en formularios](forms-based-authentication.md)
- [Prepararse para publicar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

