---
title: Constantes MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e35760ddb20f40a176d789be2db6c282fac05af8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586308"
---
# <a name="mapi-constants"></a>Constantes MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene las definiciones de constantes, declaraciones de interfaz MAPI y los identificadores de clase e interfaz usados por la API de MAPI.
  
## <a name="class-and-interface-identifiers"></a>Identificadores de clase e interfaz

Use la macro DEFINE_GUID definida en el guiddef.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar los nombres simbólicos de identificador único global (GUID) con sus valores, a menos que se indique lo contrario.
  
## <a name="attachment-security-conversion-api"></a>La API de conversión de seguridad de datos adjuntos

Esta sección contiene las definiciones de constantes y los identificadores de interfaz para la API de seguridad de datos adjuntos.
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

Use la macro MAPIMETHOD definida en el mapidefs.h de archivo de encabezado de Windows SDK para definir la función virtual pura **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**. 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

Use la macro DECLARE_MAPI_INTERFACE_ definida en el mapidefs.h de archivo de encabezado de Windows SDK para definir la tabla de método virtual para **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**. 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a>La API de conversión de MIME a MAPI

Esta sección contiene las definiciones de constantes y los identificadores de clase e interfaz de la API de conversión de MIME a MAPI.
  
### <a name="constants"></a>Constantes

|||
|:-----|:-----|
|CCSF_SMTP  <br/> |0x0002  <br/> |
|CCSF_NOHEADERS  <br/> |0x0004  <br/> |
|CCSF_USE_TNEF  <br/> | 0x0010  <br/> |
|CCSF_INCLUDE_BCC  <br/> |0 x 0020  <br/> |
|CCSF_8BITHEADERS  <br/> | 0x0040  <br/> |
|CCSF_USE_RTF  <br/> |0 x 0080  <br/> |
|CCSF_PLAIN_TEXT_ONLY  <br/> |0 x 1000  <br/> |
|CCSF_NO_MSGID  <br/> |0 x 4000  <br/> |
|E_INVALIDARG  <br/> | *Tal como se define en el archivo winerror.h archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows*  <br/> |
   
### <a name="class-identifiers"></a>Identificadores de clase

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a>Identificadores de interfaz

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a>API de estado sin conexión

Esta sección contiene las definiciones de constantes y los identificadores de clase e interfaz de la API de estado sin conexión.
  
### <a name="constants"></a>Constantes

|||
|:-----|:-----|
|E_INVALIDARG  <br/> | *Tal como se define en el archivo winerror.h archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows*  <br/> |
|E_NOINTERFACE  <br/> | *Tal como se define en el archivo winerror.h archivo de encabezado de Windows (SDK)*  <br/> |
|MAPIOFFLINE_ADVISE_DEFAULT  <br/> |0 (ULONG)  <br/> |
|MAPIOFFLINE_UNADVISE_DEFAULT  <br/> |0 (ULONG)  <br/> |
|MAPIOFFLINE_ADVISE_TYPE_STATECHANGE  <br/> |1  <br/> |
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |0 x 1  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |0 x 2  <br/> |
|MAPIOFFLINE_FLAG_BLOCK  <br/> |0 x 00002000  <br/> |
|MAPIOFFLINE_FLAG_DEFAULT  <br/> |0x00000000  <br/> |
|MAPIOFFLINE_STATE_ALL  <br/> |0x003f037f  <br/> |
|**En línea o sin conexión** <br/> ||
|MAPIOFFLINE_STATE_OFFLINE_MASK  <br/> |0 x 00000003  <br/> |
|MAPIOFFLINE_STATE_OFFLINE  <br/> |0x00000001  <br/> |
|MAPIOFFLINE_STATE_ONLINE  <br/> |0x00000002  <br/> |
   
### <a name="class-identifiers"></a>Identificadores de clase

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a>Identificadores de interfaz

```cpp
//{000672B5-0000-0000-c000-000000000046}
DEFINE_GUID(IID_IMAPIOffline, 0x000672B5, 0x0000, 0x0000, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
```

```cpp
//{0317bde5-fc29-44cd-8dcd-36125a3be9ec}
DEFINE_GUID(IID_IMAPIOfflineNotify, 0x0317bde5, 0xfc29, 0x44cd, 0x8d, 0xcd, 0x36, 0x12, 0x5a, 0x3b, 0xe9, 0xec);
```

```cpp
//{42175607-ff3e-4790-bc18-66c8643e6424
DEFINE_GUID(IID_IMAPIOfflineMgr, 0x42175607, 0xFF3E, 0x4790, 0xbc, 0x18, 0x66, 0xc8, 0x64, 0x3e, 0x64, 0x24);
```

## <a name="outlook-named-properties"></a>Propiedades con nombre de Outlook

Esta sección contiene las definiciones de constantes para las propiedades con nombre y su espacio de nombres y las otras constantes relacionadas.
  
### <a name="definitions-for-named-properties"></a>Definiciones de propiedades con nombre

```cpp
#define dispidMeetingType0x0026 
#define dispidFileUnder0x8005 
#define dispidYomiFirstName 0x802C 
#define dispidYomiLastName 0x802D 
#define dispidYomiCompanyName 0x802E 
#define dispidWorkAddressStreet 0x8045 
#define dispidWorkAddressCity 0x8046 
#define dispidWorkAddressState 0x8047 
#define dispidWorkAddressPostalCode 0x8048 
#define dispidWorkAddressCountry 0x8049 
#define dispidWorkAddressPostOfficeBox 0x804A 
#define dispidInstMsg 0x8062 
#define dispidEmailDisplayName 0x8080 
#define dispidEmailAddrType 0x8082 
#define dispidEmailEmailAddress 0x8083 
#define dispidEmailOriginalDisplayName 0x8084 
#define dispidEmail1OriginalEntryID0x8085 
#define dispidEmail2DisplayName 0x8090 
#define dispidEmail2AddrType 0x8092 
#define dispidEmail2EmailAddress 0x8093 
#define dispidEmail2OriginalDisplayName 0x8094 
#define dispidEmail2OriginalEntryID0x8095 
#define dispidEmail3DisplayName 0x80A0 
#define dispidEmail3AddrType 0x80A2 
#define dispidEmail3EmailAddress 0x80A3 
#define dispidEmail3OriginalDisplayName 0x80A4 
#define dispidEmail3OriginalEntryID0x80A5 
#define dispidTaskStatus 0x8101 
#define dispidTaskStartDate 0x8104 
#define dispidTaskDueDate 0x8105 
#define dispidTaskActualEffort 0x8110 
#define dispidTaskEstimatedEffort 0x8111 
#define dispidTaskFRecur 0x8126 
#define dispidBusyStatus0x8205 
#define dispidLocation 0x8208 
#define dispidApptStartWhole 0x820D 
#define dispidApptEndWhole 0x820E 
#define dispidApptDuration 0x8213 
#define dispidRecurring 0x8223 
#define dispidTimeZoneStruct0x8233 
#define dispidAllAttendeesString 0x8238 
#define dispidToAttendeesString 0x823B 
#define dispidCCAttendeesString 0x823C 
#define dispidConfCheck0x8240 
#define dispidApptCounterProposal 0x8257 
#define dispidApptTZDefStartDisplay0x825E 
#define dispidApptTZDefEndDisplay0x825F 
#define dispidApptTZDefRecur0x8260 
#define dispidReminderTime0x8502 
#define dispidReminderSet 0x8503 
#define dispidFormStorage0x850F 
#define dispidPageDirStream0x8513 
#define dispidSmartNoAttach 0x8514 
#define dispidCommonStart 0x8516 
#define dispidCommonEnd 0x8517 
#define dispidFormPropStream0x851B 
#define dispidRequest 0x8530 
#define dispidCompanies 0x8539 
#define dispidContacts0x853A 
#define dispidPropDefStream0x8540 
#define dispidScriptStream0x8541 
#define dispidCustomFlag0x8542 
#define dispidReminderNextTime 0x8560 
#define dispidHeaderItem0x8578 
#define dispidUseTNEF0x8582 
#define dispidToDoTitle0x85A4 
#define dispidLogType 0x8700 
#define dispidLogStart 0x8706 
#define dispidLogDuration 0x8707 
#define dispidLogEnd 0x8708 
```

### <a name="definitions-for-namespaces"></a>Definiciones de espacios de nombres

Los siguientes identificadores únicos (globales GUID) representan los espacios de nombres de las propiedades con nombre.
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment= {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

Hacer referencia a la sección almacén MAPI para las definiciones de PSETID.
  
### <a name="other-constants"></a>Otras constantes

|||
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0xD000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x2000000  <br/> |
|MNID_ID  <br/> | *Tal como se define en el mapidefs.h del archivo de encabezado.*  <br/> |
|MNID_STRING  <br/> | *Tal como se define en el mapidefs.h del archivo de encabezado.*  <br/> |
|mtgNone  <br/> |0 x 0  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |
|mtgFullUpdate  <br/> |0 x 00010000  <br/> |
|mtgInfoUpdate  <br/> |0 x 00020000  <br/> |
|mtgOutofDate  <br/> |0 x 00080000  <br/> |
|mtgDelegated  <br/> |0 x 00100000  <br/> |
   
## <a name="replication-api"></a>API de replicación

Esta sección contiene las definiciones de constantes, declaraciones de interfaz MAPI e identificadores de clase e interfaz para la API de replicación.
  
### <a name="constants"></a>Constantes

La siguiente es una estructura [MAPIUID](mapiuid.md) que identifica un proveedor de servicios MAPI: 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|DNH_OK  <br/> |0 x 00010000  <br/> |
|DNT_OK  <br/> |0 x 00010000  <br/> |
|HSF_LOCAL  <br/> |0 x 00000008  <br/> |
|HSF_COPYDESTRUCTIVE  <br/> |0 x 00000010  <br/> |
|HSF_OK  <br/> |0 x 00010000  <br/> |
|MDB_OST_LOGON_UNICODE  <br/> |((ULONG) 0X00000800)  <br/> |
|MDB_OST_LOGON_ANSI  <br/> |((ULONG) 0 X 00001000)  <br/> |
|SHOW_SOFT_DELETES  <br/> |((ULONG) 0 X 00000002)  <br/> |
|SS_ACTIVE  <br/> |0  <br/> |
|SS_SUSPENDED  <br/> |1  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |
|SYNC_OUTGOING_MAIL  <br/> |0 x 00000200  <br/> |
|SYNC_BACKGROUND  <br/> |0 x 00001000  <br/> |
|SYNC_THESE_FOLDERS  <br/> |0 x 00020000  <br/> |
|SYNC_HEADERS  <br/> |0x02000000  <br/> |
|UPC_OK  <br/> |0 x 00010000  <br/> |
|UPD_ASSOC  <br/> |0x00000001  <br/> |
|UPD_MOV  <br/> |0x00000002  <br/> |
|UPD_OK  <br/> |0 x 00010000  <br/> |
|UPD_MOVED  <br/> |0 x 00020000  <br/> |
|UPD_UPDATE  <br/> |0 x 00040000  <br/> |
|UPD_COMMIT  <br/> |0 x 00080000  <br/> |
|UPF_NEW  <br/> |0x00000001  <br/> |
|UPF_MOD_PARENT  <br/> |0x00000002  <br/> |
|UPF_MOD_PROPS  <br/> |0 x 00000004  <br/> |
|UPF_DEL  <br/> |0 x 00000008  <br/> |
|UPF_OK  <br/> |0 x 00010000  <br/> |
|UPH_OK  <br/> |0 x 00010000  <br/> |
|UPM_ASSOC  <br/> |0x00000001  <br/> |
|UPM_NEW  <br/> |0x00000002  <br/> |
|UPM_MOV  <br/> |0 x 00000004  <br/> |
|UPM_MOD_PROPS  <br/> |0 x 00000008  <br/> |
|UPM_HEADER  <br/> |0 x 00000010  <br/> |
|UPM_OK  <br/> |0 x 00010000  <br/> |
|UPM_MOVED  <br/> |0 x 00020000  <br/> |
|UPM_COMMIT  <br/> |0 x 00040000  <br/> |
|UPM_DELETE  <br/> |0 x 00080000  <br/> |
|UPM_SAVE  <br/> |0 x 00100000  <br/> |
|UPR_ASSOC  <br/> |0x00000001  <br/> |
|UPR_READ  <br/> |0x00000002  <br/> |
|UPR_OK  <br/> |0 x 00010000  <br/> |
|UPR_COMMIT  <br/> |0 x 00020000  <br/> |
|UPS_UPLOAD_ONLY  <br/> |0x00000001  <br/> |
|UPS_DNLOAD_ONLY  <br/> |0x00000002  <br/> |
|UPS_ONE_FOLDER  <br/> |0 x 00000004  <br/> |
|UPS_THESE_FOLDERS  <br/> |0x00000080  <br/> |
|UPS_OK  <br/> |0 x 00010000  <br/> |
|UPT_OK  <br/> |0 x 00010000  <br/> |
|UPT_PUBLIC  <br/> |0x00000001  <br/> |
|UPV_ERROR  <br/> |0 x 00010000  <br/> |
|UPV_DIRTY  <br/> |0 x 00020000  <br/> |
|UPV_COMMIT  <br/> |0 x 00040000  <br/> |
   
### <a name="interface-declarations"></a>Declaraciones de interfaz

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a>Identificadores de interfaz

```cpp
//{4FDEEFF0-0319-11CF-B4CF-00AA0DBBB6E6}
DEFINE_GUID (IID_IPSTX, 0x4FDEEFF0, 0x0319, 0x11CF, 0xB4, 0xCF, 0x00, 0xAA, 0x0D, 0xBB, 0xB6, 0xE6)
```

```cpp
//{2067A790-2A45-11D1-EB86-00A0C90DCA6D}
DEFINE_GUID (IID_IPSTX2, 0x2067A790, 0x2A45, 0x11D1, 0xEB, 0x86, 0x00, 0xA0, 0xC9, 0x0D, 0xCA, 0x6D)
```

```cpp
//{55f15320-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX3, 0x55f15320, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{aa2e2092-ac08-11d2-a2f9-0060b0ec3d4f}
DEFINE_GUID (IID_IPSTX4, 0xaa2e2092, 0xac08, 0x11d2, 0xa2, 0xf9, 0x00, 0x60, 0xb0, 0xec, 0x3d, 0x4f)
```

```cpp
//{55f15322-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX5, 0x55f15322, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{55f15323-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX6, 0x55f15323, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{d2d85db4-840f-49b8-9982-07d2405ec6b7}
DEFINE_GUID (IID_IOSTX, 0xd2d85db4,  0x840f, 0x49b8, 0x99, 0x82, 0x07, 0xd2, 0x40, 0x5e, 0xc6, 0xb7)
```

<br/>

Usar los siguientes dos identificadores de interfaz con [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md)o [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir y pasar por alto cualquier verificación proveedor en un objeto de carpeta y un objeto de mensaje, respectivamente. 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a>Almacén de MAPI

Esta sección contiene las definiciones de constantes y los identificadores de interfaz usan las API de dicha interfaz con un almacén de MAPI.
  
### <a name="constants"></a>Constantes

||||
|:-----|:-----|:-----|
|fnevIndexing  <br/> |((ULONG) 0 X 00010000)  <br/> |Un proveedor de almacén puede especificar **fnevIndexing** en el miembro **ulEventType** de la estructura de **[notificación](notification.md)** para notificar el indizador que un objeto está preparado para la indización. El miembro de la **información** de la estructura de **notificación** contiene una estructura **[EXTENDED_NOTIFICATION](extended_notification.md)** .  <br/> |
|FS_NONE  <br/> |0 x 00  <br/> |Un cliente puede llamar a **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** y verificación de la máscara de bits devuelto. **FS_NONE** indica que la carpeta no es compatible con el uso compartido.  <br/> |
|FS_SUPPORTS_SHARING  <br/> |0x01  <br/> |Un cliente puede llamar a **IFolderSupport::GetSupportMask** y verificación de la máscara de bits devuelto. **FS_SUPPORTS_SHARING** indica que la carpeta es compatible con el uso compartido.  <br/> |
|INDEXING_SEARCH_OWNER  <br/> |((ULONG) 0 X 00000001)  <br/> |Identifica el proceso que es inserción de una notificación en un indizador que un objeto está preparado para la indización.  <br/> |
|MNID_ID  <br/> |Tal como se define en el mapidefs.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows  <br/> |Un valor para el campo **ulKind** de la estructura **[MAPINAMEID](mapinameid.md)** .  <br/> |
|MNID_STRING  <br/> |Tal como se define en el mapidefs.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows.  <br/> |Un valor para el campo **ulKind** de la estructura **[MAPINAMEID](mapinameid.md)** .  <br/> |
|MSCAP_RES_ANNOTATION  <br/> |((ULONG) 0 X 00000001)  <br/> |Si un cliente especifica **MSCAP_SEL_RESTRICTION** en *mscapSelector* para **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** puede devolver este valor si el almacén de pasa por alto los parámetros no válidos en una restricción.  <br/> |
|MSCAP_SECURE_FOLDER_HOMEPAGES  <br/> |((ULONG) 0 X 00000020)  <br/> |Si un cliente especifica **MSCAP_SEL_FOLDER** en *mscapSelector* para **IMSCapabilities::GetCapabilities**, **GetCapabilities** puede devolver este valor si el almacén es un almacén no predeterminada que es compatible con las páginas principales de carpeta.  <br/> |
|STORE_PUSHER_OK  <br/> |((ULONG) 0X00800000)  <br/> |Un cliente puede obtener la propiedad **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** para determinar las características de un almacén de mensajes. Si el proveedor de almacenamiento establece la marca **STORE_PUSHER_OK** en la máscara de bits, que significa que el controlador de protocolo MAPI no va a rastrear el almacén y el almacén es responsable de los cambios a través de notificaciones de inserción al indizador para que los mensajes se indizan.  <br/> |
   
### <a name="definitions-for-namespaces"></a>Definiciones de espacios de nombres

Los siguientes identificadores únicos (globales GUID) representan los espacios de nombres de propiedades con nombre. Que se indizan por el controlador de protocolo MAPI (PH) y se documentan como de solo lectura.
  
> [!CAUTION]
> Las propiedades con nombre no deben usarse para crear o modificar elementos. 
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment   = {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting       = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

#### <a name="mnidid-properties"></a>Propiedades MNID_ID
  
```cpp
// In PSETID_Address
#define dispidWorkAddressStreet 0x8045
#define dispidWorkAddressCity 0x8046
#define dispidWorkAddressState 0x8047
#define dispidWorkAddressPostalCode 0x8048
#define dispidWorkAddressCountry 0x8049
#define dispidInstMsg 0x8062
#define dispidEmailDisplayName 0x8080
#define dispidEmailOriginalDisplayName 0x8084
```

```cpp
// In PSETID_Appointment
#define dispidLocation 0x8208
#define dispidApptStartWhole 0x820D
#define dispidApptEndWhole 0x820E
#define dispidApptDuration 0x8213
#define dispidRecurring 0x8223
#define dispidAllAttendeesString 0x8238
#define dispidToAttendeesString 0x823B
#define dispidCCAttendeesString 0x823C
```

```cpp
// In PSETID_Common
#define dispidReminderSet 0x8503
#define dispidSmartNoAttach 0x8514
#define dispidCommonStart 0x8516
#define dispidCommonEnd 0x8517
#define dispidRequest 0x8530
#define dispidCompanies 0x8539
#define dispidReminderNextTime 0x8560
```

```cpp
// In PSETID_Log (also known as Journal)
#define dispidLogType 0x8700
#define dispidLogStart 0x8706
#define dispidLogDuration 0x8707
#define dispidLogEnd 0x8708MNID_STRING properties
```

```cpp
// In PSETID_Task
#define dispidTaskStartDate 0x8104
#define dispidTaskDueDate 0x8105
#define dispidTaskActualEffort 0x8110
#define dispidTaskEstimatedEffort 0x8111
#define dispidTaskFRecur 0x8126
```

#### <a name="mnidstring-properties"></a>Propiedades MNID_STRING
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a>Identificadores de interfaz

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

Usar el `DEFINE_OLEGUID` macro definida en el guiddef.h de archivo de encabezado de Windows SDK para asociar el nombre simbólico de GUID siguiente con su valor. 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a>Constantes de la libreta de direcciones de MAPI

Esta sección contiene las definiciones de constantes para la libreta de direcciones de MAPI.
  
### <a name="constants"></a>Constantes

||||
|:-----|:-----|:-----|
|CONTAB_ROOT  <br/> |((ULONG) 0 X 00000001)  <br/> |La carpeta raíz de un objeto de la libreta de direcciones MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |((ULONG) 0 X 00000002)  <br/> |Una subcarpeta dentro de la carpeta raíz del objeto de la libreta de direcciones MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |((ULONG) 0 X 00000003)  <br/> |Un objeto de contenedor de libreta de direcciones.  <br/> |
|CONTAB_USER  <br/> |((ULONG) 0 X 00000004)  <br/> |Un objeto de usuario de mensajer�a.  <br/> |
|CONTAB_DISTLIST  <br/> |((ULONG) 0 X 00000005)  <br/> |Un objeto de lista de distribuci�n.  <br/> |
   
## <a name="additional-mapi-constants"></a>Constantes MAPI adicionales

Esta sección contiene las definiciones de constantes incluidos los códigos de error y los identificadores de interfaz usados por las API de MAPI que anteriormente no se han expuesto y se documentan.
  
||||
|:-----|:-----|:-----|
|DIALOG_MODAL  <br/> |((ULONG) 0 X 00000001)  <br/> |Cuando un cliente llama al método de [IAddrBook::Details](iaddrbook-details.md) , el cliente debe establecer la marca **DIALOG_MODAL** en el parámetro _ulFlags_ para mostrar el cuadro de diálogo modal que muestra los detalles acerca de una entrada de la libreta de direcciones determinada. Esta constante se define en mapidefs.h.  <br/> |
|ITEMPROC_FORCE  <br/> |0x00000800  <br/> |En Outlook 2007, almacenes de archivos PST ajustados tengan reglas y filtrado de spam procesa en nuevos mensajes antes de que los clientes MAPI reciben notificaciones de los mensajes nuevos. Un proveedor o cliente mediante el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para crear un nuevo mensaje en almacenes de PST debe establecer la marca **ITEMPROC_FORCE** en el parámetro _ulFlags_ del método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para indicar a PST almacén de que el mensaje es apto para las reglas de procesamiento antes de que el almacén notifica a cualquier cliente de escucha de la llegada del nuevo mensaje. Tenga en cuenta que esas reglas de procesamiento sólo se aplica a los nuevos mensajes creados en un servidor que no es un servidor de Exchange de Microsoft, debido a que Exchange Server procesa las reglas para los mensajes en el servidor. Por lo tanto, el proveedor o cliente que crea el mensaje debe pasar esta marca en combinación con **NON_EMS_XP_SAVE**, que indica que el servidor no es un servidor de Exchange.  <br/> |
| MAPI_BG_SESSION  <br/> |0x00200000  <br/> |Un cliente puede llamar a la función [MAPILogonEx](mapilogonex.md) , al establecer el indicador **MAPI_BG_SESSION** en el parámetro _flFlags_ para iniciar una sesión y realizar cualquier operación en segundo plano. En general, si un cliente se va a realizar el procesamiento en un subproceso de fondo o en un proceso independiente de manera que sea discreto al subproceso de primer plano, debe llamar a [MAPILogonEx](mapilogonex.md) con la marca **MAPI_BG_SESSION** . Un ejemplo donde se utiliza es una aplicación de cliente, como un motor de indización, abrir un archivo de carpetas personales (PST) para el acceso de tipo de fondo.  <br/> |
|MAPI_CACHE_ONLY  <br/> |0x00004000  <br/> |Un cliente puede llamar al método [IAddrBook::OpenEntry](iaddrbook-openentry.md) , al establecer el indicador **MAPI_CACHE_ONLY** en el parámetro _ulFlags indicado_ para abrir una entrada de la libreta de direcciones y tener acceso a él posteriormente sólo desde la memoria caché. Un ejemplo donde se utiliza es una aplicación cliente que desea abrir la lista Global de direcciones en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.  <br/> |
|MAPI_DIALOG_MODELESS  <br/> |0x0000000C  <br/> |Este valor se puede pasar a la función MAPISendMail de Simple MAPI en el parámetro _ulFlags_ para especificar que se muestra un cuadro de diálogo no modal mediante la aplicación de correo predeterminada. Si se establece este indicador ni MAPI_DIALOG (0 x 00000008), no se muestra ningún cuadro de diálogo.  <br/> |
|MAPI_NO_CACHE  <br/> |0 x 00000200  <br/> |Si Microsoft Office Outlook está en modo caché de Exchange y un almacén se ha abierto en modo en caché, puede llamar a un proveedor de servicio o cliente de [IMsgStore::OpenEntry](imsgstore-openentry.md), al establecer el indicador **MAPI_NO_CACHE** en el parámetro _ulFlags_ para abrir un elemento o una carpeta en el almacén remoto. Tenga en cuenta que si se abre el almacén de mensajes con el indicador **MDB_ONLINE** en el servidor remoto, no es necesario usar el indicador **MAPI_NO_CACHE** .  <br/> |
|MAPI_UNICODE.  <br/> |0 x 80000000  <br/> |Un proveedor de servicio o cliente puede llamar a la función [OpenIMsgOnIStg](openimsgonistg.md) , establecer el indicador **MAPI_UNICODE** en el parámetro _ulFlags_ para crear archivos .msg de Unicode. El resultante [IMessage: IMAPIProp](imessageimapiprop.md) archivo muestra **STORE_UNICODE_OK** en su [Propiedad canónico PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) y es compatible con propiedades de Unicode. Esta constante se define en mapidefs.h.  <br/> |
|MDB_ONLINE  <br/> |0 x 00000100  <br/> |Si Outlook está en modo caché de Exchange, un proveedor de servicio o cliente puede llamar al método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) , al establecer el indicador **MDB_ONLINE** en el parámetro _ulFlags_ para invalidar la conexión con el almacén de mensajes local y abrir el almacén en el servidor remoto. Tenga en cuenta que no se puede abrir un almacén de Exchange en modo de caché y en modo sin caché al mismo tiempo en la misma sesión MAPI. Si ya ha abierto el almacén de mensajes almacenados en caché, ya sea debe cerrar el almacén antes de que se abra con esta marca, o se abre una nueva sesión MAPI donde puede abrir el almacén de Exchange en el servidor remoto mediante el uso de esta marca.  <br/> |
|NON_EMS_XP_SAVE  <br/> |0 x 00001000  <br/> |Un cliente puede llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , al establecer el indicador **NON_EMS_XP_SAVE** en el parámetro _ulFlags_ para indicar que no se ha entregado el mensaje desde un servidor de Exchange. Este indicador se debe usar en combinación con el indicador **ITEMPROC_FORCE** en el parámetro _ulFlags_ para indicar a un almacén de archivos PST que el mensaje es apto para las reglas de procesamiento antes de la PST almacén notifica a cualquier cliente de escucha de la llegada de la Mensaje. Esta regla de procesamiento sólo se aplica a los nuevos mensajes que se crean con [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en un servidor que no es un servidor de Exchange (en cuyo caso el servidor de Exchange ya habría procesa las reglas en el mensaje).  <br/> |
|SPAMFILTER_ONSAVE  <br/> |0x00000080  <br/> |Un cliente puede llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md), al establecer el indicador **SPAMFILTER_ONSAVE** en el parámetro _ulFlags_ para habilitar spam filtrado en un mensaje que se va a guardar. Soporte técnico de filtrado de correo no está disponible sólo si el tipo de dirección de correo electrónico del remitente es el protocolo Simple de transferencia de correo (SMTP) y el mensaje se guarda en un almacén para un archivo de carpetas personales (PST).  <br/> |
|STORE_ITEMPROC  <br/> |0x00200000  <br/> |Si este indicador se establece en la [Propiedad canónico PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) de un almacén de archivos PST ajustado, indica que cuando llegue un nuevo mensaje en el almacén, el almacén tiene reglas y filtrado de spam procesa por separado en el mensaje. El almacén, a continuación, llama a [IMAPISupport::Notify](imapisupport-notify.md), establezca **fnevNewMail** en la estructura de [notificación](notification.md) que se pasa como un parámetro y pase los detalles del mensaje nuevo a un cliente de escucha. Posteriormente, cuando el cliente escucha recibe la notificación, no se procesará las reglas en el mensaje.  <br/> |
|STORE_UNICODE_OK  <br/> |0 x 00040000  <br/> |Si este indicador se incluye en la [Propiedad canónico PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), indica que el almacén admite el almacenamiento de Unicode. Un cliente puede buscar la presencia de la marca de decidir si va a solicitar o guardar información de Unicode en el repositorio.  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a>Definiciones de elementos en una carpeta de archivado

Las siguientes definiciones de constantes son valores que se usan para establecer la [Propiedad canónico PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a>Definiciones para mostrar objetos remotos

Las siguientes definiciones de constante y la macro se utilizan para mostrar objetos remotos. Para obtener más información, vea la [Propiedad canónico PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).
  
```cpp
#define DTE_FLAG_REMOTE_VALID0x80000000 
#define DTE_FLAG_ACL_CAPABLE    0x40000000 
#define DTE_MASK_REMOTE        0x0000ff00 
#define DTE_MASK_LOCAL        0x000000ff 
  
#define DTE_IS_REMOTE_VALID(v)(!!((v) & DTE_FLAG_REMOTE_VALID)) 
#define DTE_IS_ACL_CAPABLE(v)(!!((v) & DTE_FLAG_ACL_CAPABLE)) 
#define DTE_REMOTE(v)(((v) & DTE_MASK_REMOTE) >> 8) 
#define DTE_LOCAL(v)((v) & DTE_MASK_LOCAL) 
  
#define DT_ROOM((ULONG) 0x00000007) 
#define DT_EQUIPMENT((ULONG) 0x00000008) 
#define DT_SEC_DISTLIST((ULONG) 0x00000009)
```

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a>Las definiciones de la libreta de direcciones de Exchange y mensaje almacenan los códigos de error

El siguiente contiene las definiciones de código de error para la libreta de direcciones de Exchange y el almacén de mensajes, que tienen la capacidad de reconexión. La última llamada a un catálogo Global (GC) desconectados puede provocar el error **MAPI_E_END_OF_SESSION** , que sería necesario volver a intentar. 
  
MAPI admite reconexión de Outlook con un servidor de catálogo global sin reconfiguración especial, pero algún otro error códigos se pueden devolver al cliente.
  
||||
|:-----|:-----|:-----|
|MAPI_E_END_OF_SESSION  <br/> |0x80040200  <br/> |Se devuelve cuando se ha desconectado una conexión.  <br/> |
|MAPI_E_RECONNECTED  <br/> |0 x 80040125  <br/> |Se devuelve cuando el símbolo (token) de conexión de llamada a procedimiento remoto (RPC) no está actualizado. Si el símbolo (token) de la transacción actual es diferente del símbolo (token) de la conexión que significa que se ha vuelto a conectar, por lo que **MAPI_E_RECONNECTED** se devuelve y se puede tratar de la misma como **MAPI_E_END_OF_SESSION**. Debe volver a intentar la llamada.  <br/> |
|MAPI_E_OFFLINE  <br/> |0x80040126  <br/> |Se devuelve cuando la conexión está sin conexión. Normalmente, esto significa que ha ocurrido algo en el entorno, como errores del servidor o la pérdida de conectividad de red. Este error es más probable que se producen cuando se usa el modo caché de un perfil y si se intenta omitir la memoria caché para comunicarse con el servidor. Si la memoria caché nunca pudo establecer inicialmente una conexión con el servidor, puede ser en el estado sin conexión en el que podría exponer **MAPI_E_OFFLINE** .  <br/> |
   
Ninguno de los dos errores anteriores se devolverán en todos los escenarios donde es probable que aparecerían que se debe aplicar. En la mayoría de los casos, **MAPI\_E_NETWORK_ERROR** o se devolverá **MAPI_E_CALL_FAILED** . Ninguno de ellos aparecerá mediante la descarga de [Microsoft Exchange Server MAPI Client y Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) . 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a>Cuotas de modo de caché de las definiciones para el buzón de correo de Exchange Server

Las siguientes definiciones de constantes usadas por Microsoft Outlook 2010 y Microsoft Outlook 2013 para establecer el intercambio en caché las cuotas de perfil de modo que son equivalentes a las cuotas de buzón de correo de Exchange en caso contrario, sólo está disponibles con un perfil en línea.
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

Estas propiedades se asignan a sus propiedades en línea consultará y contienen los mismos valores en kilobytes. PR_QUOTA_WARNING se asigna a PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND a PR_QUOTA_PROHIBIT_SEND_QUOTA y PR_QUOTA_RECEIVE a PR_PROHIBIT_RECEIVE_QUOTA.
  
### <a name="definitions-for-message-format"></a>Definiciones de formato de mensaje

Las definiciones de constantes siguientes son valores que se usan para establecer la [Propiedad canónico PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a>Definiciones para el uso de RPC sobre HTTP

Vea el tema de la [Propiedad canónico PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) para las definiciones de constantes utiliza como indicadores para establecer la propiedad. 
  
Vea el tema de la [Propiedad canónico PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) para las definiciones de constantes que se usa para establecer la propiedad. 
  
### <a name="identifiers"></a>Identificadores

Usar el `DEFINE_OLEGUID` macro definida en el guiddef.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar los nombres simbólicos de GUID siguientes con sus valores. 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

Es el identificador siguiente para la sección de perfil de Capone de una libreta de direcciones, que contiene una propiedad [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) que desactiva efectivamente el valor predeterminado de apoyo a varios buzones de Exchange ([MultiEx](using-multiple-exchange-accounts.md)) contenedor especificado por [SetDefaultDir](iaddrbook-setdefaultdir.md).
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a>Identificadores de interfaz

#### <a name="imapisync"></a>IMAPISync
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a>IMAPISyncProgressCallback
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a>IID_IContabAdmin
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a>IID_IMAPISECUREMESSAGE
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a>IID_IMAPIGetSession
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a>Identificadores de interfaz de controlador de invalidar PST

#### <a name="iidipstoverridereq"></a>IID_IPSTOVERRIDEREQ
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a>IID_IPSTOVERRIDE1
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a>Recursos adicionales

- [Información sobre las adiciones de MAPI](about-mapi-additions.md) 
- [Información sobre las propiedades con nombre que usa Outlook](about-named-properties-used-by-outlook.md)
- [Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Administrar un mensaje en un OST sin invocar una sincronización en el modo de intercambio en caché](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

