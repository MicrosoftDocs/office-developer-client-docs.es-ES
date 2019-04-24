---
title: Crear un perfil de Outlook con MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI proporciona acceso a los almacenes de MAPI para facilitar la investigación de problemas de Exchange y Outlook y proporcionar a los programadores compatibilidad para el desarrollo de MAPI.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345993"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Crear un perfil de Outlook con MFCMAPI

MFCMAPI proporciona acceso a los almacenes de MAPI para facilitar la investigación de problemas de Exchange y Outlook y proporcionar a los programadores compatibilidad para el desarrollo de MAPI.

**Hace referencia a**: Office 365 | Outlook | Outlook 2016 
  
Para los usuarios que no son desarrolladores, se recomienda usar la interfaz de usuario de Outlook para crear perfiles para Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Configurar un perfil de Outlook con MFCMAPI

1. Abra [MFCMAPI](https://mfcmapi.codeplex.com/)y, en el menú **perfil** , haga clic en **Mostrar perfiles**. 
    
2. En el menú **acciones** , haga clic en **crear perfil**. 
    
3. Cree un nuevo nombre para el perfil y, a continuación, haga clic en **Aceptar**. 
    
4. Haga clic con el botón secundario en el nuevo perfil y, a continuación, en el menú **servicios** , haga clic en **Agregar servicio**. 
    
5. Desactive la casilla "Mostrar la interfaz de usuario del servicio" y, a continuación, haga clic en **Aceptar**. 
    
6. Haga doble clic en el perfil que acaba de crear y, a continuación, haga clic en el servicio **MSEMS** . 
    
7. Busque la sección Perfil de Exchange.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Este valor se necesitará en el paso 9.
    
8. Haga doble clic en el servicio **MSEMS** . 
    
9. Busque la sección de Perfil de **Exchange** mediante el UID del paso 7 y, a continuación, haga clic en el mismo para seleccionar la fila. 
    
10. En el menú de propiedades, haga clic en **propiedades adicionales**. 
    
11. Haga clic en **Agregar**y, a continuación, agregue las siguientes propiedades: 
    
    **para Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` y`PR_DISPLAY_NAME_W`
    
    **para Outlook para Office 365**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE`, y`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **para Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME`,, y `PR_PROFILE_AUTH_PACKAGE`. 
    
12. Haga clic en **Aceptar**y, a continuación, configure cada propiedad de acuerdo con la tabla siguiente, en función de la versión a la que se conecte. 
    
13. En el menú **sesión** , haga clic en **iniciar sesión y mostrar almacén**y, a continuación, seleccione el perfil (si aún no está seleccionado). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Property** <br/> |**Tag** <br/> |**Descripción** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |Dirección SMTP del usuario  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |El nombre para mostrar del usuario  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Configure el valor de esta propiedad, que se encuentra en la sección **EMSMDB** , y actualice el UID correspondiente para la propiedad correspondiente.  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook para Office 365
  
||||
|:-----|:-----|:-----|
|**Propiedad** <br/> |**Value** <br/> |**Descripción** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de buzón  <br/> |El alias para el buzón de correo de destino; por ejemplo, administrador  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |identificador de servidor personalizado  <br/> |Valor recuperado de la **detección automática**. con el formato <guid>@tenant. onmicrosoft.com; por ejemplo, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nodo detección automática* : respuesta/cuenta/protocolo/servidor (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |Outlook.Office365.com  <br/> | *Nodo detección automática* : respuesta/cuenta/protocolo/servidor (expr) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0X2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Contiene la configuración de un perfil usado por Outlook para conectarse a Microsoft Exchange Server mediante una llamada a procedimiento remoto (RPC) sobre el protocolo de transferencia de hiperTexto (HTTP). *Nodo detección automática* : respuesta/cuenta/protocolo/SSL (expr) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |Representa el protocolo de autenticación que se usará para este *nodo de detección automática* de perfiles: respuesta/cuenta/protocolo/AUTHPACKAGE (expr) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0X0)  <br/> |Describe el esquema de autenticación que se debe usar para el *nodo de detección automática* de RPC: Response/Account/Protocol/AUTHPACKAGE (EXCH)) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Elemento CertPrincipalName  <br/> |Se usa para admitir la autenticación mutua; por ejemplo, msstd:Outlook. com *Autodiscover node* : Response/Account/Protocol/CERTPRINCIPALNAME (expr)) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Propiedad** <br/> |**Value** <br/> |**Descripción** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |alias de buzón  <br/> |El alias para el buzón de correo de destino; por ejemplo, administrador  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |identificador de servidor personalizado  <br/> |Valor recuperado de la **detección automática**. con el formato <guid>@tenant. onmicrosoft.com; por ejemplo, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Nodo detección automática* : respuesta/cuenta/protocolo/servidor (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | nombre de dominio del servidor de acceso de cliente  <br/> | El nombre de dominio completo (FQDN); por ejemplo, *nodo de detección automática* de E2013cas.contoso.com: respuesta/cuenta/protocolo/servidor (expr) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |Contiene la configuración de un perfil usado por Outlook para conectarse a Microsoft Exchange Server mediante una llamada a procedimiento remoto (RPC) en el *nodo detección automática* del Protocolo de transferencia de hipertexto (http): respuesta/cuenta/protocolo/SSL (expr) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0X2)  <br/> |Representa el protocolo de autenticación que se usará para este *nodo de detección automática* de perfiles: respuesta/cuenta/protocolo/AUTHPACKAGE (expr) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |Describe el esquema de autenticación que se debe usar para el *nodo de detección automática* de RPC: Response/Account/Protocol/AUTHPACKAGE (EXCH)) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Todos los valores de propiedad mencionados anteriormente pueden variar para su organización concreta. 
> - <sup>1</sup> debe usar la versión Unicode en lugar de la versión ANSI. 
> - Debe usar la detección automática basada en XML (POX) sin formato. Esta es la única detección automática admitida para configurar los perfiles de Outlook/Exchange.
> - Puede usar Outlook para realizar una solicitud de detección automática en su nombre haciendo clic con el botón secundario en el icono de Outlook de la **bandeja del sistema**, mientras mantiene presionada la tecla Ctrl y haciendo clic en **probar configuración automática del correo electrónico**. 
> - Para PR_ROH_FLAGS, es posible que el entorno requiera la marca ROHFLAGS_SSL_ONLY (0X2) para indicar a MAPI que use solo SSL. Si su entorno requiere la autenticación mutua, tendrá que establecer la marca también [ROHFLAGS_MUTUAL_AUTH (0x4)]. Para establecer ROHFLAGS_MUTUAL_AUTH (0x4), es necesario que también establezca la propiedad PR_ROH_PROXY_PRINCIPAL_NAME. Debe establecer este valor en el nombre principal del servidor.
> - <sup>2</sup> para Outlook 2010, tendrá que usar el protocolo expr. Outlook 2013 usa el protocolo exHTTP. 
> - <sup>3</sup> es posible que este valor no esté en la respuesta de detección automática. Si no se especifica, el cliente debe usar Kerberos o NTLM. 
    
Para obtener sugerencias de solución de problemas, consulte [How to Configure an Outlook Profile Using MFCMAPI for Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Vea también

- [Referencia MAPI de Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Crear mediante programación un perfil en Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

