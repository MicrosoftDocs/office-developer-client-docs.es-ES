---
title: Buscar el historial de descarga de mensajes de una cuenta POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: En este tema se describe cómo un cliente de correo puede obtener acceso a la propiedad PidTagAttachDataBinary para obtener el historial de descarga de mensajes para una cuenta POP3.
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399561"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Buscar el historial de descarga de mensajes de una cuenta POP3

En este tema se describe cómo un cliente de correo puede obtener acceso a la propiedad [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) para obtener el historial de descarga de mensajes para una cuenta POP3. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>¿Por qué obtener el historial de descarga de mensajes?

El proveedor de protocolo de oficina de correos (POP) para Outlook permite a los usuarios para recuperar y descargar nuevos mensajes de correo electrónico en su dispositivo local y posteriormente dejar o eliminar estos mensajes de correo electrónico en el servidor de correo. Cuando el cliente de correo comprobaciones para que nuevos mensajes descargar, debe ser capaz de identificar y descargue sólo los mensajes nuevos para esa bandeja de entrada. Para ello, el cliente de correo usar primero el comando UIDL (listado de identificador único), que obtiene un mapa de cada mensaje que nunca se ha entregado a esa bandeja de entrada a un identificador único (UID). El cliente también obtiene el historial de descarga de mensajes para los mensajes que se han descargado o eliminado de la Bandeja de entrada en la que el cliente. Con el mapa UID de mensaje y el historial de descarga, el cliente, a continuación, puede identificar los mensajes que no están presentes en el historial de como nuevo y, por tanto, que debe descargarse.
  
Para obtener el historial de descarga de mensajes para una bandeja de entrada:
  
- Siga los pasos descritos en este tema para buscar la propiedad **PidTagAttachDataBinary** , que contiene el historial de un objeto binario grande (BLOB) que sigue a un formato específico. 
    
- Continuar con el [análisis el historial de descarga de mensajes de una cuenta POP3](parsing-the-message-download-history-for-a-pop3-account.md), que se describe cómo analizar este BLOB para identificar los mensajes que se han descargado o eliminado para esa bandeja de entrada.
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Conceptos básicos necesarios para localizar el mensaje el historial de descarga

El historial de descarga de mensajes para una bandeja de entrada se almacena en una propiedad MAPI binaria, **PidTagAttachDataBinary**, en los datos adjuntos de un mensaje oculto en la Bandeja de entrada. La tabla 1 muestra los recursos para los conceptos que le ayudarán a comprender cómo localizar el mensaje de historial de descarga.
  
**Tabla 1. Conceptos básicos**

|**Título del artículo**|**Descripción**|
|:-----|:-----|
|[Carpetas de MAPI oculto](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI permite a los clientes de correo almacenar información en carpetas ocultas y mensajes ocultos. Carpetas ocultas se encuentran en la parte asociada de carpetas MAPI y normalmente contienen información que no es visible para y no a los usuarios pueden manipular. Los clientes decidir el formato y el contenido para almacenar en los mensajes ocultos en las carpetas ocultas.  <br/> |
|[Mensajes MAPI](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI almacena los mensajes en las carpetas, ya sea en el subárbol IPM estándar que es visible para los usuarios de un cliente, o fuera del subárbol e invisibles para los usuarios. Los mensajes pueden tener datos adicionales que se almacenan en un archivo adjunto, que puede encontrarse en el formulario de un archivo, otro mensaje o un objeto OLE. En el caso de historial de descarga de mensaje, el historial se almacena en una propiedad de un mensaje que se adjunta a otro mensaje oculto.  <br/> |
|[Información general de propiedades de mensaje](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Cuando un cliente almacena información en un mensaje, en realidad almacena la información en una propiedad del mensaje. MAPI es compatible con muchas propiedades: algunas siempre existen y se pueden establecer por los clientes, otros son opcionales, y los clientes no se prevé que van a estar disponible o se establece a los valores válidos. El historial de descarga de mensajes se almacena en la propiedad **PidTagAttachDataBinary** de un archivo adjunto a un mensaje oculto.  <br/> |
|[Perfiles de MAPI](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |En tiempo de inicio de sesión en una sesión, el cliente de correo selecciona un perfil que describe los servicios y los proveedores que se va a utilizar. Un perfil se divide en las secciones que contienen propiedades. En concreto, las propiedades de [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) y [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) siempre existen. Clave de búsqueda de un perfil es único entre todos los perfiles y se almacena en la sección de perfil que se identifica con **MUID_PROFILE_INSTANCE** (que se define en MAPIGUID. (H). Utilice [IMAPISession::OpenProfileSection](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) para abrir la sección y [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) para obtener los valores de propiedad.  <br/> |
|[Tablas de contenido](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Los proveedores de almacén de mensajes implementan las tablas de contenido para sus carpetas. Para los mensajes ocultos en la parte asociada de una carpeta, los proveedores de almacén de mensajes admiten tablas de contenido asociados y clientes pueden utilizar el método [IMAPIContainer::GetContentsTable](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) para devolver un puntero a la tabla de contenido asociada.  <br/> |
|[Información sobre las restricciones](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Tipos de restricciones](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Crear una restricción](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Código de restricción de muestra](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |En MAPI, los clientes pueden utilizar restricciones para filtrar las tablas de contenido, para buscar las filas que representan los mensajes que tienen una determinada propiedad establecida en un valor específico. Las restricciones se definen mediante el uso de la estructura de datos [SRestriction](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) , que puede contener una unión de las estructuras de restricción más especializadas. El método [IMAPITable:: FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) aplica una restricción y recupera la primera fila en una tabla que coincida con los criterios de restricción.  <br/> |
|[Información sobre el registro de almacenes de indexación](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |Use la propiedad [PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) para comprobar el tipo de proveedor de almacenamiento. Por ejemplo, para comprobar si un almacén es un almacén de Exchange, la propiedad **PidTagStoreProvider** debe devolver un valor representado por la constante **pbExchangeProviderPrimaryUserGuid**, que se define en el edkmdb.h del archivo de encabezado público.  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Localizar el mensaje oculto adecuado y datos adjuntos

Ahora que sabemos que el historial de descarga de mensajes para una bandeja de entrada se encuentra en la propiedad **PidTagAttachDataBinary** de un archivo adjunto a un mensaje oculto, el procedimiento para localizar los datos adjuntos adecuados del mensaje oculto apropiado implica lo siguiente procedimientos: 
  
1. [Busque el mensaje oculto adecuado](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [Encontrar los datos adjuntos adecuados del mensaje oculto](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [Obtener acceso a la propiedad PidTagAttachDataBinary de los datos adjuntos del mensaje](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Busque el mensaje oculto adecuado

1. Obtener la propiedad [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) desde el perfil, en la sección de perfil especificada por **MUID_PROFILE_INSTANCE**.
    
2. Abra el contenido asociado para la carpeta Bandeja de entrada mediante una llamada a **IMAPIContainer::GetContentsTable**.
    
3. Crear una restricción en función del [PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**), **PidTagSearchKey** (**PR_SEARCH_KEY**) y las propiedades de [PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) para obtener una tabla que contiene todos los mensajes ocultos en el contenido de asociados de la Bandeja de entrada. El siguiente es un ejemplo de una restricción extraída de [localizar el historial de UIDL de POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx).
    
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

4. De la tabla, busque el mensaje oculto mediante el uso de **IMAPITable:: FindRow**.
    
5. Si se produce un error en el paso 4 buscar un mensaje oculto, cambie la restricción para usar **PidTagSearchKey** (**PR_SEARCH_KEY**) en lugar de **PidTagConversationKey**, tal y como se muestra a continuación:
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Busque el mensaje oculto mediante **IMAPITable:: FindRow**. 
    
7. Si se produce un error en el paso 6, cambie la restricción para usar [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) que se va a igual que el valor siguiente (se muestra a continuación utilizando `printf` estilo sustitución por razones de brevedad). 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Busque el mensaje oculto mediante el uso de **IMAPITable:: FindRow**.
    
9. Si está ejecutando Outlook 2010 o una versión posterior, use los siguientes valores para **PidTagProfileName** (**PR_PROFILE_NAME**) y **PidTagSearchKey** (**PR_SEARCH_KEY**), respectivamente.
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Ejecute a través de los pasos del 3 al 8. Si se produce un error buscar un mensaje, retroceder a los pasos 3 a 8 originales.
    
10. Abra el mensaje oculto que se encuentra en el paso 4, 6 u 8.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Encontrar los datos adjuntos adecuados del mensaje oculto

Debido a que el mensaje oculto puede tener más de un dato adjunto, busque los datos adjuntos adecuado en el orden siguiente.
  
> [!NOTE]
> Este procedimiento se usa nuevamente la `printf` estilo sustitución por razones de brevedad. 

1. Buscar datos adjuntos cuya [PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) coincide con la cadena siguiente, donde `szEmailAddress` es la dirección del usuario SMTP, tal como se especifica en el perfil del usuario. . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Buscar datos adjuntos cuya [PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) coincide con "BlobPOP %s", `szEmailAddress`.
    
3. Buscar datos adjuntos cuya [PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) coincide con "BlobPOP %s", `szEmailAddress`.
    
4. Buscar datos adjuntos cuya **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) coincide con "Blob%.8x", `dwAcctUID`, donde `dwAcctUID` proviene de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md). Puede usar el método [IOlkAccount::GetProp](iolkaccount-getprop.md) para obtener acceso a la propiedad **PROP_ACCT_MINI_UID** . 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Obtener acceso a la propiedad PidTagAttachDataBinary de los datos adjuntos del mensaje

Después de encontrar los datos adjuntos de mensaje adecuado del mensaje oculto, use **IMAPIProp::GetProps** para leer la propiedad **PidTagAttachDataBinary** de los datos adjuntos. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Siguientes pasos

Ha aprendido de este tema buscar el historial de descarga de mensajes de la Bandeja de entrada de un cliente de correo POP3. Vea [el historial de descarga de mensajes de una cuenta POP3 de análisis](parsing-the-message-download-history-for-a-pop3-account.md) para aprender a analizar este historial para identificar los mensajes que se han descargado o eliminado de la Bandeja de entrada. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>Vea también

- [Administrar la descarga de mensajes de las cuentas POP3](managing-message-downloads-for-pop3-accounts.md)   
- [Analizar el historial de descarga de mensajes de una cuenta POP3](parsing-the-message-download-history-for-a-pop3-account.md)
- [Localizar el historial UIDL de POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

