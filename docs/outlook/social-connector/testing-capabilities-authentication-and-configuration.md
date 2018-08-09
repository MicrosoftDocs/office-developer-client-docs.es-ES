---
title: Probar las funciones, la autenticación y la configuración
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: En este tema se describe las pruebas de introducción, características y escenarios de configuración de una cuenta y la autenticación de un usuario para una red social.
ms.openlocfilehash: ac294291e2226dbb73f822b2a641fe2bf67ce5eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821218"
---
# <a name="testing-capabilities-authentication-and-configuration"></a>Probar las funciones, la autenticación y la configuración

En este tema se describe las pruebas de introducción, características y escenarios de configuración de una cuenta y la autenticación de un usuario para una red social.
  
## <a name="getting-capabilities"></a>Introducción a las funciones

Un proveedor de Outlook Social Connector (OSC) implementa [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)y las llamadas OSC **GetCapabilities** para obtener la funcionalidad admitida por el proveedor. Las capacidades que es compatible con su proveedor para su red social deben conocidas en el momento de la implementación y no dependen de una llamada a la red social en tiempo real. Por ejemplo, los usuarios de Outlook pueden iniciar Outlook sin conexión y **GetCapabilities** no se basan en la conectividad de red en el momento cuando se inicia Outlook. 
  
Cuando se prueba el proveedor, debe comprobar que el parámetro de cadena de _los resultados_ devuelto por **GetCapabilities** se ajusta del elemento **capabilities** , tal como se define por el esquema XML de proveedor OSC. Para obtener más información, vea [Los elementos XML de las capacidades](capabilities-xml-elements.md).
  
## <a name="configuring-an-account"></a>Configuración de una cuenta

Cuando el OSC configura una cuenta, debe comprobar si se muestran el icono de redes sociales y el nombre, y que los hipervínculos crear cuenta y contraseña olvidado aparecen en el cuadro de diálogo de configuración de cuenta como especificado por el proveedor.
  
### <a name="social-network-icon-and-name"></a>Nombre y el icono de redes sociales

Después de obtener acceso a las funciones, puede continuar el OSC para obtener el icono y el nombre para la red social llamando a [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) y [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md). Realice las siguientes pruebas para comprobar que se realizan con éxito estas llamadas al método.
  
|**Elemento que se va a probar**|**Comportamiento esperado**|
|:-----|:-----|
|Icono de redes sociales  <br/> | El icono de redes sociales se muestra correctamente en los siguientes lugares en el OSC:  <br/>  En el cuadro de diálogo OSC para **Las cuentas de red Social**.  <br/>  En el menú desplegable al intentar agregar a una persona como amigo.  <br/>  En la tarjeta de identificación cuando se siguen un amigo.  <br/> <br/>**Nota**: puede tener acceso al cuadro de diálogo para **Las cuentas de red Social** haciendo clic en la ficha **Ver** en Outlook, en el grupo del **Panel de personas** , haciendo clic en **Panel de personas**y, a continuación, haga clic en **Configuración de la cuenta**.           |
|Nombre de la red social  <br/> | El nombre de red social se muestra correctamente en los siguientes lugares en el OSC:  <br/>  En el cuadro de diálogo OSC para **Las cuentas de red Social**.  <br/>  En el menú desplegable al intentar agregar a una persona como amigo.  <br/>  Como el título del cuadro de diálogo contraseña cuando intenta cambiar la contraseña existente.  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a>Hipervínculos que muestra en el cuadro de diálogo de configuración

Después de llamar a **ISocialProvider::GetCapabilities**, el OSC usa el valor del elemento **hideHyperlinks** en el parámetro de _resultados_ para determinar si se debe mostrar u ocultar el **olvidó y **haga clic aquí para crear una cuenta de** su contraseña?** hipervínculos en el cuadro de diálogo de configuración de cuenta. Compruebe si **hideHyperlinks** es **false**, la configuración de cuenta muestra estas direcciones URL.
  
### <a name="support-to-create-account"></a>Soporte técnico para crear la cuenta

Compruebe si el parámetro de _los resultados_ de la llamada al método **ISocialProvider::GetCapabilities** tiene el elemento **hideHyperlinks** establece en **false** y el elemento de **createAccountUrl** establecido en **true**, al hacer clic en la dirección URL se abre la página en el explorador web predeterminado.
  
### <a name="support-for-forgotten-password"></a>Compatibilidad con contraseña olvidado

Compruebe si el parámetro de _los resultados_ de la llamada al método **ISocialProvider::GetCapabilities** tiene el elemento **hideHyperlinks** establece en **false** y el elemento de **forgotPasswordUrl** establecido en **true**, al hacer clic en la dirección URL se abre la página en el explorador web predeterminado.
  
## <a name="authenticating-users"></a>Autenticación de usuarios

Probar los siguientes escenarios independientemente de si su proveedor de OSC admite la autenticación básica o autenticación basada en formularios.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|Inicio de sesión por primera vez.  <br/> |Correctamente, el usuario puede iniciar sesión en la red social.  <br/> |
|Inicio de sesión con una contraseña consta de una variedad de caracteres, incluidos los signos de puntuación y caracteres Unicode.  <br/> |Correctamente, el usuario puede iniciar sesión en la red social, independientemente del tipo de caracteres usados en la contraseña.  <br/> |
|El cuadro de diálogo para mostrar el nombre de usuario o el identificador de **Cuentas de red Social**  <br/> |Después de que el usuario ha iniciado sesión correctamente en la red, cuadro de diálogo de OSC para **Las cuentas de red Social** muestra el nombre de usuario que ha iniciado la sesión o un identificador.  <br/> |
|Se produce un error en la autenticación.  <br/> |El OSC muestra el error en el **nombre de usuario no válido o la contraseña**.  <br/> |
|No se puede conectar a la red social.  <br/> |El OSC muestra el error **no se encuentra el servidor**.  <br/> |
|Ser capaz de recuperar elementos.  <br/> |Una vez que el usuario se ha autenticado, se deberían permitir todas las actividades. No hay errores obtener datos amigos o las actividades.  <br/> |
|Inicie sesión en la red social después de reiniciar Outlook.  <br/> |Si el proveedor OSC permite que el almacenamiento en caché de la contraseña, una vez autenticado el usuario la primera vez, el usuario no se pide posteriormente las credenciales cada vez que el OSC intenta obtener datos desde la red social.  <br/> |
   
Además, si su proveedor de OSC admite la autenticación basada en formularios, pruebe para el siguiente escenario.
  
|**Escenario**|**Comportamiento esperado**|
|:-----|:-----|
|La introducción de una dirección URL a un formulario para el usuario para iniciar sesión desde una llamada a [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md)OSC.  <br/> |El OSC abre la dirección URL en el explorador del usuario de forma predeterminada, y la página Web permite al usuario que escriba las credenciales para iniciar sesión en la red social.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de capacidades](capabilities-xml-elements.md)  
- [Autenticación básica](basic-authentication.md) 
- [Autenticación basada en formularios](forms-based-authentication.md)
- [Prepararse liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

