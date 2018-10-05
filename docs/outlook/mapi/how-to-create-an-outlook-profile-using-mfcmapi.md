---
title: Crear un perfil de Outlook con MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI proporciona acceso a los almacenes MAPI para facilitar la investigación de problemas de Exchange y Outlook y para proporcionar a los desarrolladores con compatibilidad para el desarrollo de MAPI.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397880"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Crear un perfil de Outlook con MFCMAPI

MFCMAPI proporciona acceso a los almacenes MAPI para facilitar la investigación de problemas de Exchange y Outlook y para proporcionar a los desarrolladores con compatibilidad para el desarrollo de MAPI.

**Hace referencia a**: Office 365 | Outlook | Outlook 2016 
  
Para que no sean los desarrolladores, se recomienda que use la interfaz de usuario de Outlook para crear perfiles de Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Configurar un perfil de Outlook con MFCMAPI

1. Abra [MFCMAPI](https://mfcmapi.codeplex.com/)y, en el menú de **perfil** , haga clic en **Mostrar perfiles**. 
    
2. En el menú **acciones** , haga clic en **Crear perfil**. 
    
3. Crear un nuevo nombre para el perfil y, a continuación, haga clic en **Aceptar**. 
    
4. Haga clic en el nuevo perfil y, a continuación, en el menú de **Servicios** , haga clic en **Agregar servicio**. 
    
5. Desactive la casilla "Interfaz de usuario de servicio para mostrar" y, a continuación, haga clic en **Aceptar**. 
    
6. Haga doble clic en el perfil recién creado y, a continuación, haga clic en el servicio **MSEMS** . 
    
7. Busque la sección de perfil de Exchange.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Necesitará este valor en el paso 9.
    
8. Haga doble clic en el servicio **MSEMS** . 
    
9. Busque la sección de perfil de **Exchange** utilizando el UID del paso 7 y, a continuación, haga clic para seleccionar la fila. 
    
10. En el menú de la propiedad, haga clic en **Propiedades adicionales**. 
    
11. Haga clic en **Agregar**y, a continuación, agregue las siguientes propiedades: 
    
    **Para Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` y`PR_DISPLAY_NAME_W`
    
    **Para Outlook para Office 365**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, `PR_PROFILE_AUTH_PACKAGE`, y`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Para Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, y `PR_PROFILE_AUTH_PACKAGE`. 
    
12. Haga clic en **Aceptar**y, a continuación, configure cada propiedad de acuerdo con la tabla siguiente, dependiendo de la versión que se va a conectar. 
    
13. En el menú **sesión** , haga clic en **Inicio de sesión y almacén para mostrar**y, a continuación, seleccione el perfil (si aún no está seleccionado). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Propiedad** <br/> |**Tag** <br/> |**Descripción** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |Dirección SMTP del usuario  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |El nombre para mostrar del usuario  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Configurar el valor de esta propiedad, que se encuentra en la sección **EMSMDB** y actualizar el UID correspondiente para la propiedad coincidente  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook para Office 365
  
||||
|:-----|:-----|:-----|
|**Propiedad** <br/> |**Valor** <br/> |**Descripción** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de buzón de correo  <br/> |El alias del buzón de destino; Por ejemplo, Administrador  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |identificador de servidor personalizado  <br/> |El valor recuperado de **detección automática**. en el formato <guid>@tenant.onmicrosoft.com; Por ejemplo, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nodo de detección automática* : respuesta/cuenta / / servidor de protocolo (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |Outlook.office365.com  <br/> | *Nodo de detección automática* : respuesta/cuenta / / servidor de protocolo (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0 X 1)  <br/> ROH_FLAGS_USE_SSL (0 X 2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0 X 4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0 X 8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0 X 20)  <br/> |Contiene la configuración en un perfil de Outlook usado para conectarse a Microsoft Exchange Server mediante una llamada a procedimiento remoto (RPC) a través del protocolo de transferencia de hipertexto (HTTP). *Nodo de detección automática* : respuesta/cuenta/protocolo/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0 X 1)  <br/> |Representa el protocolo de autenticación que se usará para este perfil de *Nodo de detección automática* : respuesta/cuenta/protocolo/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0 X 0)  <br/> |Describe el esquema de autenticación que se usará para el *Nodo de detección automática* RPC: respuesta/cuenta/protocolo/AuthPackage (EXCH)) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Elemento CertPrincipalName  <br/> |Se utiliza para admitir la autenticación mutua; Por ejemplo, msstd:outlook.com *El nodo de detección automática* : respuesta/cuenta/protocolo/CertPrincipalName (EXPR)) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Propiedad** <br/> |**Valor** <br/> |**Descripción** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de buzón de correo  <br/> |El alias del buzón de destino; Por ejemplo, Administrador  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |identificador de servidor personalizado  <br/> |El valor recuperado de **detección automática**. en el formato <guid>@tenant.onmicrosoft.com; Por ejemplo, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nodo de detección automática* : respuesta/cuenta / / servidor de protocolo (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | nombre de dominio de servidor de acceso de cliente  <br/> | El nombre de dominio completo (FQDN); Por ejemplo, e2013cas.contoso.com *El nodo de detección automática* : servidor/Protocolo o cuenta/respuesta (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0 X 1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0 X 8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0 X 20))  <br/> |Contiene la configuración en un perfil de Outlook usado para conectarse a Microsoft Exchange Server mediante una llamada a procedimiento remoto (RPC) a través del protocolo de transferencia de hipertexto (HTTP) *Nodo de detección automática* : respuesta/cuenta/protocolo/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0 X 2)  <br/> |Representa el protocolo de autenticación que se usará para este perfil de *Nodo de detección automática* : respuesta/cuenta/protocolo/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0XA)  <br/> |Describe el esquema de autenticación que se usará para el *Nodo de detección automática* RPC: respuesta/cuenta/protocolo/AuthPackage (EXCH)) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Todos los valores de propiedad mencionados anteriormente pueden variar para su organización en particular. 
> - <sup>1</sup> debe usar la versión de Unicode en lugar de la versión ANSI. 
> - Debe usar el XML antigua (POX) sin formato en función de detección automática. Esto es la única de detección automática compatible para configurar los perfiles de Outlook y Exchange.
> - Puede utilizar Outlook para realizar una solicitud de detección automática en su nombre haciendo doble clic en el icono de Outlook en la **Bandeja del sistema**, mientras se mantiene presionada la tecla CTRL y haciendo clic en **Configuración automática de correo electrónico de prueba**. 
> - Para PR_ROH_FLAGS, su entorno puede requerir la marca ROHFLAGS_SSL_ONLY (0 x 2) para indicar a MAPI sólo usen SSL. Si su entorno requiere autenticación mutua, debe establecer esa marca así como [ROHFLAGS_MUTUAL_AUTH (0 x 4)]. Configuración de ROHFLAGS_MUTUAL_AUTH (0 x 4) requerirá que también establezca la propiedad PR_ROH_PROXY_PRINCIPAL_NAME. Debe establecer esta opción para ser el nombre de entidad de seguridad del servidor.
> - <sup>2</sup> para Outlook 2010, deberá usar el protocolo EXPR. Outlook 2013 usa el protocolo EXHTTP. 
> - <sup>3</sup> este valor no puede ser en la respuesta de detección automática. Si no se especifica, el cliente debe utilizar Kerberos o NTLM. 
    
Sugerencias para resolver problemas, vea [cómo configurar un perfil de Outlook con MFCMAPI para Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Vea también

- [Referencia MAPI de Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Crear mediante programación un perfil en Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

