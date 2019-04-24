---
title: Buscar el historial de descarga de mensajes de una cuenta POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: En este tema se describe cómo un cliente de correo puede obtener acceso a la propiedad PidTagAttachDataBinary para obtener el historial de descargas de mensajes de una cuenta POP3.
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321878"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Buscar el historial de descarga de mensajes de una cuenta POP3

En este tema se describe cómo un cliente de correo puede obtener acceso a la propiedad [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) para obtener el historial de descargas de mensajes de una cuenta POP3. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>¿Por qué se obtiene el historial de descargas de mensajes?

El proveedor de protocolo de oficina de correos (POP) para Outlook permite a los usuarios recuperar y descargar nuevos mensajes de correo electrónico en su dispositivo local y, posteriormente, dejar o eliminar estos mensajes de correo electrónico en el servidor de correo. Cuando el cliente de correo comprueba si hay mensajes nuevos que descargar, tiene que poder identificar y descargar sólo los mensajes nuevos para esa bandeja de entrada. El cliente de correo lo hace primero usando el comando UIDL (Unique ID Listing), que obtiene un mapa de cada mensaje que se ha entregado alguna vez en la bandeja de entrada a un identificador único (UID). El cliente también obtiene el historial de descargas de mensajes para los mensajes que se han descargado o eliminado para la bandeja de entrada de ese cliente. Con el mapa UID del mensaje y el historial de descargas, el cliente puede identificar los mensajes que están ausentes en el historial como nuevos y, por lo tanto, debe descargarlos.
  
Para obtener el historial de descargas de mensajes de una bandeja de entrada:
  
- Siga los pasos de este tema para buscar la propiedad **PidTagAttachDataBinary** , que contiene el historial en un objeto binario grande (BLOB) que sigue a un formato específico. 
    
- Continúe con [el análisis del historial de descarga de mensajes de una cuenta POP3](parsing-the-message-download-history-for-a-pop3-account.md), que describe cómo analizar este BLOB para identificar los mensajes que se han descargado o eliminado para esa bandeja de entrada.
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Conceptos básicos que deben conocerse para encontrar el historial de descargas de mensajes

El historial de descarga de mensajes de una bandeja de entrada se almacena en una propiedad MAPI binaria, **PidTagAttachDataBinary**, en datos adjuntos de un mensaje oculto en la bandeja de entrada. La tabla 1 muestra los recursos para conocer los conceptos que le ayudarán a encontrar el historial de descargas de mensajes.
  
**Tabla 1. Conceptos básicos**

|**Título del artículo**|**Description**|
|:-----|:-----|
|[Carpetas ocultas MAPI](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI permite que los clientes de correo almacenen información en carpetas ocultas y mensajes ocultos. Las carpetas ocultas están en la parte asociada de las carpetas MAPI y normalmente contienen información que no es visible para que la manipulen los usuarios. Los clientes deciden el formato y el contenido que se almacenarán en las carpetas ocultas en los mensajes ocultos.  <br/> |
|[Mensajes MAPI](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI almacena los mensajes en carpetas, ya sea en el subárbol IPM estándar que es visible para los usuarios de un cliente o fuera del subárbol y no es visible para los usuarios. Los mensajes pueden tener datos adicionales almacenados en datos adjuntos, que pueden tener el formato de un archivo, otro mensaje o un objeto OLE. En el caso del historial de descarga de mensajes, el historial se almacena en una propiedad de un mensaje adjunto a otro mensaje oculto.  <br/> |
|[Información general de propiedades de mensaje](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Cuando un cliente almacena información en un mensaje, en realidad se almacena la información en una propiedad del mensaje. MAPI admite muchas propiedades: algunos siempre existen y los pueden configurar los clientes, otros son opcionales y los clientes no pueden esperar que estén disponibles o se establezcan en valores válidos. El historial de descargas de mensajes se almacena en la propiedad **PidTagAttachDataBinary** de datos adjuntos en un mensaje oculto.  <br/> |
|[Perfiles MAPI](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |En el momento de inicio de sesión en una sesión, el cliente de correo selecciona un perfil que describe los proveedores y los servicios que se van a usar. Un perfil se divide en secciones que contienen propiedades. En concreto, las propiedades [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) y [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) siempre existen. La clave de búsqueda de un perfil es única entre todos los perfiles y se almacena en la sección de perfil identificada por **MUID_PROFILE_INSTANCE** (que se define en MAPIGUID. H). Use [IMAPISession:: OpenProfileSection](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) para abrir la sección y use [IMAPIProp:: GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) para obtener los valores de la propiedad.  <br/> |
|[Tablas de contenido](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Los proveedores de almacenamiento de mensajes implementan tablas de contenido para sus carpetas. Para los mensajes ocultos en la parte asociada de una carpeta, los proveedores de almacenamiento de mensajes admiten tablas de contenido asociadas y los clientes pueden usar el método [IMAPIContainer:: GetContentsTable](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) para devolver un puntero a la tabla de contenido asociada.  <br/> |
|[Acerca de las restricciones](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Tipos de restricciones](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Creación de una restricción](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Ejemplo de código de restricción](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |En MAPI, los clientes pueden usar restricciones para filtrar tablas de contenido, para buscar filas que representen los mensajes que tienen una propiedad determinada establecida en un valor específico. Las restricciones se definen mediante la estructura de datos [SRestriction](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) , que puede contener una Unión de estructuras de restricción más especializadas. El método [IMAPITable:: FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) aplica una restricción y recupera la primera fila de una tabla que coincida con los criterios de restricción.  <br/> |
|[Acerca del registro de almacenes para la indización](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |Use la propiedad [PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) para comprobar el tipo de proveedor de almacenamiento. Por ejemplo, para comprobar si un almacén es un almacén de Exchange, la propiedad **PidTagStoreProvider** debe devolver un valor representado por la constante **pbExchangeProviderPrimaryUserGuid**, que se define en el archivo de encabezado público edkmdb. h.  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Buscar el mensaje y los datos adjuntos ocultos apropiados

Ahora que sabemos que el historial de descarga de mensajes de una bandeja de entrada está en la propiedad **PidTagAttachDataBinary** de datos adjuntos en un mensaje oculto, el procedimiento para buscar los datos adjuntos adecuados del mensaje oculto apropiado implica lo siguiente: los 
  
1. [Buscar el mensaje oculto apropiado](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [Buscar el archivo adjunto apropiado del mensaje oculto](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [Obtener acceso a la propiedad PidTagAttachDataBinary de los datos adjuntos del mensaje](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Buscar el mensaje oculto apropiado

1. Obtenga la propiedad [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) del perfil, en la sección de perfil especificada por **MUID_PROFILE_INSTANCE**.
    
2. Abra el contenido asociado a la carpeta Bandeja de entrada llamando a **IMAPIContainer:: GetContentsTable**.
    
3. Cree una restricción basada en las propiedades [PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**) **, PidTagSearchKey** (**PR_SEARCH_KEY**) y [PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) para obtener una tabla que contiene todos los mensajes ocultos en el contenido asociado de la bandeja de entrada. El siguiente es un ejemplo de una restricción que se extrae [al buscar el historial de UIDL de POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx).
    
   ```cpp
      SRestriction rgRes[3]; 
      SPropValue rgProps[3]; 
      rgRes[0].rt = RES_AND; 
      rgRes[0].res.resAnd.cRes = 2; 
      rgRes[0].res.resAnd.lpRes = &amp;rgRes[1]; 
      rgRes[1].rt = RES_PROPERTY; 
      rgRes[1].res.resProperty.relop = RELOP_EQ; 
      rgRes[1].res.resProperty.ulPropTag = PR_CONVERSATION_KEY; 
      rgRes[1].res.resProperty.lpProp = &amp;rgProps[0]; 
      rgRes[2].rt = RES_PROPERTY; 
      rgRes[2].res.resProperty.relop = RELOP_EQ; 
      rgRes[2].res.resProperty.ulPropTag = PR_MESSAGE_CLASS; 
      rgRes[2].res.resProperty.lpProp = &amp;rgProps[1]; 
      rgProps[0].ulPropTag = PR_CONVERSATION_KEY; 
      rgProps[0].Value.bin = pVals[iSearchKey].Value.bin; // PR_SEARCH_KEY from the profile 
      rgProps[1].ulPropTag = PR_MESSAGE_CLASS; 
      rgProps[1].Value.LPSZ = (LPTSTR)"IPM.MessageManager";
   ```

4. En la tabla, busque el mensaje oculto mediante **IMAPITable:: FindRow**.
    
5. Si el paso 4 no encuentra un mensaje oculto, cambie la restricción para usar **PidTagSearchKey** (**PR_SEARCH_KEY**) en lugar de **PidTagConversationKey**, tal como se muestra a continuación:
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Buscar el mensaje oculto mediante **IMAPITable:: FindRow**. 
    
7. Si se produce un error en el paso 6, cambie la restricción para que use [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) sea igual que el `printf` siguiente valor (que se muestra a continuación con sustitución de estilo para mayor brevedad). 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Busque el mensaje oculto mediante **IMAPITable:: FindRow**.
    
9. Si está ejecutando Outlook 2010 o una versión posterior, use los siguientes valores para **PidTagProfileName** (**PR_PROFILE_NAME**) y **PidTagSearchKey** (**PR_SEARCH_KEY**), respectivamente.
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Realice los pasos 3 a 8. Si no encuentra un mensaje, revierte a los pasos originales 3 a 8.
    
10. Abra el mensaje oculto que se encuentra en el paso 4, 6 u 8.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Buscar el archivo adjunto apropiado del mensaje oculto

Como el mensaje oculto puede tener más de un archivo de datos adjuntos, busque el archivo adjunto apropiado en el siguiente orden.
  
> [!NOTE]
> De nuevo, este procedimiento `printf` usa la sustitución de estilo para mayor brevedad. 

1. Busque datos adjuntos cuyo [PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) coincida con la siguiente cadena `szEmailAddress` , donde es la dirección SMTP del usuario, como se especifica en el perfil del usuario. . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Busque datos adjuntos cuyo [PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) coincida con "BlobPOP% s `szEmailAddress`",.
    
3. Busque datos adjuntos cuyo [PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) coincida con "BlobPOP% s `szEmailAddress`",.
    
4. Busque datos adjuntos cuyo **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) coincida con "BLOB%. 8x `dwAcctUID`", `dwAcctUID` , donde proviene de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md). Puede usar el método [IOlkAccount:: GetProp](iolkaccount-getprop.md) para obtener acceso a la propiedad **PROP_ACCT_MINI_UID** . 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Obtener acceso a la propiedad PidTagAttachDataBinary de los datos adjuntos del mensaje

Una vez que haya encontrado el mensaje adjunto al mensaje oculto, use **IMAPIProp:: GetProps** para leer la propiedad **PidTagAttachDataBinary** de los datos adjuntos. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Pasos siguientes

Ha aprendido en este tema cómo buscar el historial de descarga de mensajes de la bandeja de entrada de un cliente de correo POP3. Consulte [analizar el historial de descarga de mensajes de una cuenta POP3](parsing-the-message-download-history-for-a-pop3-account.md) para obtener información sobre cómo analizar este historial para identificar los mensajes que se han descargado o eliminado para la bandeja de entrada. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>Vea también

- [Administrar la descarga de mensajes de las cuentas POP3](managing-message-downloads-for-pop3-accounts.md)   
- [Analizar el historial de descarga de mensajes de una cuenta POP3](parsing-the-message-download-history-for-a-pop3-account.md)
- [Buscar el historial de UIDL de POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

