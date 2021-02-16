---
title: Crear un perfil de Outlook con MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI proporciona acceso a almacenes MAPI para facilitar la investigación de problemas de Exchange y Outlook y para proporcionar a los desarrolladores compatibilidad con el desarrollo mapi.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345993"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Crear un perfil de Outlook con MFCMAPI

MFCMAPI proporciona acceso a almacenes MAPI para facilitar la investigación de problemas de Exchange y Outlook y para proporcionar a los desarrolladores compatibilidad con el desarrollo mapi.

**Hace referencia a**: Office 365 | Outlook | Outlook 2016 
  
Para los no desarrolladores, se recomienda usar la interfaz de usuario de Outlook para crear perfiles para Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Configurar un perfil de Outlook mediante MFCMAPI

1. Abra [MFCMAPI](https://mfcmapi.codeplex.com/)y, en el menú **Perfil,** haga clic **en Mostrar perfiles.** 
    
2. En el menú **Acciones,** haga clic **en Crear perfil.** 
    
3. Cree un nuevo nombre para el perfil y, a continuación, haga clic en **Aceptar.** 
    
4. Haga clic con el botón secundario en el nuevo perfil y, a continuación, en **el** menú Servicios, haga clic en **Agregar servicio.** 
    
5. Desactive la casilla "Interfaz de usuario del servicio de visualización" y, a continuación, haga clic en **Aceptar.** 
    
6. Haga doble clic en el perfil recién creado y, a continuación, haga clic en el **servicio MSEMS.** 
    
7. Busque la sección Perfil de Exchange.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Necesitará este valor en el paso 9.
    
8. Haga doble clic en el **servicio MSEMS.** 
    
9. Busque la **sección de** perfil de Exchange mediante el UID del paso 7 y, a continuación, haga clic con un solo clic para seleccionar la fila. 
    
10. En el menú Propiedad, haga clic **en Propiedades adicionales.** 
    
11. Haga **clic en** Agregar y, a continuación, agregue las siguientes propiedades: 
    
    **Para Outlook 2016:** `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` y `PR_DISPLAY_NAME_W`
    
    **Para Outlook para Office 365:** `PR_PROFILE_UNRESOLVED_NAME` , , , , `PR_PROFILE_UNRESOLVED_SERVER` `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE` y `PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Para Exchange 2013:** `PR_PROFILE_UNRESOLVED_NAME` , , , y `PR_PROFILE_UNRESOLVED_SERVER` `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE` . 
    
12. Haga **clic en** Aceptar y, a continuación, configure cada propiedad según la tabla siguiente, en función de la versión a la que se conecte. 
    
13. En el **menú Sesión,** haga clic **en Inicio de** sesión y Mostrar almacén y, a continuación, seleccione el perfil (si aún no está seleccionado). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Propiedad** <br/> |**Tag** <br/> |**Descripción** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |Dirección SMTP del usuario  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |El nombre para mostrar del usuario  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Configure el valor de esta propiedad, que se encuentra en la sección **EMSMDB,** y actualice el UID correspondiente para la propiedad correspondiente.  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook para Office 365
  
||||
|:-----|:-----|:-----|
|**Propiedad** <br/> |**Valor** <br/> |**Descripción** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de buzón  <br/> |El alias del buzón de destino; por ejemplo, Administrador  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |id. de servidor personalizado  <br/> |El valor recuperado de **Detección automática.** en el formato <guid> @tenant.onmicrosoft.com; por ejemplo, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nodo de detección automática:*  respuesta/cuenta/protocolo/servidor (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *Nodo de detección automática:*  respuesta/cuenta/protocolo/servidor (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0x2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Contiene la configuración de un perfil usado por Outlook para conectarse a Microsoft Exchange Server mediante una llamada a procedimiento remoto (RPC) a través del protocolo de transferencia de hipertexto (HTTP). *Nodo de detección automática:*  respuesta/cuenta/protocolo/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |Representa el protocolo de autenticación que se usará para este nodo *de detección*  automática de perfil: Respuesta/Cuenta/Protocolo/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0)  <br/> |Describe el esquema de autenticación que se debe usar para el nodo *de detección*  automática de RPC: Response/Account/Protocol/AuthPackage (EXCH) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Elemento CertPrincipalName  <br/> |Se usa para admitir la autenticación mutua; por ejemplo, nodo de detección  automática msstd:outlook.com: Response/Account/Protocol/CertPrincipalName (EXPR) ) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Propiedad** <br/> |**Valor** <br/> |**Descripción** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de buzón  <br/> |El alias del buzón de destino; por ejemplo, Administrador  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |id. de servidor personalizado  <br/> |El valor recuperado de **Detección automática.** en el formato <guid> @tenant.onmicrosoft.com; por ejemplo, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nodo de detección automática:*  respuesta/cuenta/protocolo/servidor (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | nombre de dominio del servidor de acceso de cliente  <br/> | El nombre de dominio completo (FQDN); por ejemplo, e2013cas.contoso.com  *Detección automática:*  Respuesta/Cuenta/Protocolo/Servidor (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |Contiene la configuración de un perfil usado por Outlook para conectarse a Microsoft Exchange Server mediante una llamada a procedimiento remoto (RPC) a través del nodo *de*  detección automática del protocolo de transferencia de hipertexto (HTTP): respuesta/cuenta/protocolo/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0x2)  <br/> |Representa el protocolo de autenticación que se usará para este nodo *de detección*  automática de perfil: Respuesta/Cuenta/Protocolo/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |Describe el esquema de autenticación que se debe usar para el nodo *de detección*  automática de RPC: Respuesta/Cuenta/Protocolo/AuthPackage (EXCH) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Todos los valores de propiedad mencionados anteriormente pueden variar para su organización en particular. 
> - <sup>1</sup> Debe usar la versión Unicode, en lugar de la versión ANSI. 
> - Debe usar la detección automática basada en XML antiguo sin formato (POX). Esta es la única detección automática compatible para configurar perfiles de Outlook/Exchange.
> - Puede usar Outlook para realizar una solicitud de Detección automática en su nombre haciendo clic con el botón secundario en el icono de Outlook en la bandeja del **sistema,** manteniendo presionada la tecla CTRL y haciendo clic en Probar configuración automática **de correo electrónico.** 
> - Por PR_ROH_FLAGS, el entorno puede requerir la marca ROHFLAGS_SSL_ONLY (0x2) para que MAPI use solo SSL. Si su entorno requiere autenticación mutua, deberá establecer también esa marca [ROHFLAGS_MUTUAL_AUTH (0x4)]. Establecer ROHFLAGS_MUTUAL_AUTH (0x4) requerirá que también establezca la propiedad PR_ROH_PROXY_PRINCIPAL_NAME. Debe establecerlo como el nombre principal del servidor.
> - <sup>2</sup> Para Outlook 2010, tendrá que usar el protocolo EXPR. Outlook 2013 usa el protocolo EXHTTP. 
> - <sup>3</sup> Es posible que este valor no esté en la respuesta de Detección automática. Si no se especifica, el cliente debe usar Kerberos o NTLM. 
    
Para obtener sugerencias para solucionar problemas, consulte [Cómo configurar un perfil de Outlook con MFCMAPI para Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Consulte también

- [Referencia MAPI de Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Crear un perfil mediante programación en Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

