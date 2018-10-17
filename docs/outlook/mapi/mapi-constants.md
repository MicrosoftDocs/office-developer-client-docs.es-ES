---
title: Constantes MAPI
manager: soliver
ms.date: 10/02/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: Definiciones de constantes, declaraciones de interfaz MAPI e identificadores de clase e interfaz usados por las API de MAPI.
ms.openlocfilehash: 343b777550d88276a1f5cad19f12ae7fc09c6244
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393736"
---
# <a name="mapi-constants"></a>Constantes MAPI

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene las definiciones de constantes, declaraciones de interfaz MAPI e identificadores de clase e interfaz usados por las API de MAPI.
  
## <a name="class-and-interface-identifiers"></a>Identificadores de clase e interfaz

Use la macro DEFINE_GUID definida en el archivo de encabezado guiddef.h del Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar nombres simbólicos de identificador único global (GUID) con sus valores, a menos que se indique lo contrario.
  
## <a name="attachment-security-conversion-api"></a>API de conversión de seguridad de datos adjuntos

Esta sección contiene las definiciones de constantes e identificadores de interfaz de la API de seguridad de datos adjuntos
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

Utilice la macro MAPIMETHOD definida en el archivo de encabezado mapidefs.h de Windows SDK para definir la función virtual pura **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**. 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

Utilice la macro DECLARE_MAPI_INTERFACE_ definida en el archivo de encabezado mapidefs.h de Windows SDK para definir la tabla de método virtual de ** [IAttachmentSecurity](iattachmentsecurityiunknown.md)**. 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a>API de conversión de MAPI-MIME

Esta sección contiene las definiciones de constantes e identificadores de clase e interfaz para la API de conversión de MAPI-MIME.
  
### <a name="constants"></a>Constantes

|||
|:-----|:-----|
|CCSF_SMTP  <br/> |0x0002  <br/> |
|CCSF_NOHEADERS  <br/> |0x0004  <br/> |
|CCSF_USE_TNEF  <br/> | 0x0010  <br/> |
|CCSF_INCLUDE_BCC  <br/> |0x0020  <br/> |
|CCSF_8BITHEADERS  <br/> | 0x0040  <br/> |
|CCSF_USE_RTF  <br/> |0x0080  <br/> |
|CCSF_PLAIN_TEXT_ONLY  <br/> |0x1000  <br/> |
|CCSF_NO_MSGID  <br/> |0x4000  <br/> |
|CCSF_GLOBAL_MESSAGE  <br/> |0x00200000  <br/> |
|E_INVALIDARG  <br/> | *Según se define en el archivo de encabezado winerror.h del Kit de desarrollo de Software (SDK) de Microsoft Windows*  <br/> |
   
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

Esta sección contiene las definiciones de constantes e identificadores de clase e interfaz para la API de estado sin conexión.
  
### <a name="constants"></a>Constantes

|||
|:-----|:-----|
|E_INVALIDARG  <br/> | *Según se define en el archivo de encabezado winerror.h del Kit de desarrollo de Software (SDK) de Microsoft Windows*  <br/> |
|E_NOINTERFACE  <br/> | *Según se define en el archivo de encabezado winerror.h de Windows (SDK) de Windows*  <br/> |
|MAPIOFFLINE_ADVISE_DEFAULT  <br/> |(ULONG)0  <br/> |
|MAPIOFFLINE_UNADVISE_DEFAULT  <br/> |(ULONG)0  <br/> |
|MAPIOFFLINE_ADVISE_TYPE_STATECHANGE  <br/> |1  <br/> |
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |0x1  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |0x2  <br/> |
|MAPIOFFLINE_FLAG_BLOCK  <br/> |0x00002000  <br/> |
|MAPIOFFLINE_FLAG_DEFAULT  <br/> |0x00000000  <br/> |
|MAPIOFFLINE_STATE_ALL  <br/> |0x003f037f  <br/> |
|**En línea o sin conexión** <br/> ||
|MAPIOFFLINE_STATE_OFFLINE_MASK  <br/> |0x00000003  <br/> |
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

Esta sección contiene las definiciones de constantes de propiedades con nombre, sus espacios de nombres y otras constantes relacionadas.
  
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

Los siguientes identificadores únicos globales (GUID) representan los espacios de nombres de las propiedades con nombre.
  
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

Consulte la sección del almacén de MAPI para las definiciones de PSETID.
  
### <a name="other-constants"></a>Otras constantes

|||
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0xD000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x2000000  <br/> |
|MNID_ID  <br/> | *Según se define en el archivo de encabezadomapidefs.h.*  <br/> |
|MNID_STRING  <br/> | *Según se define en el archivo de encabezadomapidefs.h.*  <br/> |
|mtgNone  <br/> |0x0  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |
|mtgFullUpdate  <br/> |0x00010000  <br/> |
|mtgInfoUpdate  <br/> |0x00020000  <br/> |
|mtgOutofDate  <br/> |0x00080000  <br/> |
|mtgDelegated  <br/> |0x00100000  <br/> |
   
## <a name="replication-api"></a>API de replicación

Esta sección contiene las definiciones de constantes, declaraciones de interfaz MAPI e identificadores de clase e interfaz de la API de replicación.
  
### <a name="constants"></a>Constantes

Esta es una estructura [MAPIUID](mapiuid.md) que identifica un proveedor de servicios MAPI: 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|DNH_OK  <br/> |0x00010000  <br/> |
|DNT_OK  <br/> |0x00010000  <br/> |
|HSF_LOCAL  <br/> |0x00000008  <br/> |
|HSF_COPYDESTRUCTIVE  <br/> |0x00000010  <br/> |
|HSF_OK  <br/> |0x00010000  <br/> |
|MDB_OST_LOGON_UNICODE  <br/> |((ULONG) 0x00000800)  <br/> |
|MDB_OST_LOGON_ANSI  <br/> |((ULONG) 0x00001000)  <br/> |
|SHOW_SOFT_DELETES  <br/> |((ULONG) 0x00000002)  <br/> |
|SS_ACTIVE  <br/> |0  <br/> |
|SS_SUSPENDED  <br/> |1  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |
|SYNC_BACKGROUND  <br/> |0x00001000  <br/> |
|SYNC_THESE_FOLDERS  <br/> |0x00020000  <br/> |
|SYNC_HEADERS  <br/> |0x02000000  <br/> |
|UPC_OK  <br/> |0x00010000  <br/> |
|UPD_ASSOC  <br/> |0x00000001  <br/> |
|UPD_MOV  <br/> |0x00000002  <br/> |
|UPD_OK  <br/> |0x00010000  <br/> |
|UPD_MOVED  <br/> |0x00020000  <br/> |
|UPD_UPDATE  <br/> |0x00040000  <br/> |
|UPD_COMMIT  <br/> |0x00080000  <br/> |
|UPF_NEW  <br/> |0x00000001  <br/> |
|UPF_MOD_PARENT  <br/> |0x00000002  <br/> |
|UPF_MOD_PROPS  <br/> |0x00000004  <br/> |
|UPF_DEL  <br/> |0x00000008  <br/> |
|UPF_OK  <br/> |0x00010000  <br/> |
|UPH_OK  <br/> |0x00010000  <br/> |
|UPM_ASSOC  <br/> |0x00000001  <br/> |
|UPM_NEW  <br/> |0x00000002  <br/> |
|UPM_MOV  <br/> |0x00000004  <br/> |
|UPM_MOD_PROPS  <br/> |0x00000008  <br/> |
|UPM_HEADER  <br/> |0x00000010  <br/> |
|UPM_OK  <br/> |0x00010000  <br/> |
|UPM_MOVED  <br/> |0x00020000  <br/> |
|UPM_COMMIT  <br/> |0x00040000  <br/> |
|UPM_DELETE  <br/> |0x00080000  <br/> |
|UPM_SAVE  <br/> |0x00100000  <br/> |
|UPR_ASSOC  <br/> |0x00000001  <br/> |
|UPR_READ  <br/> |0x00000002  <br/> |
|UPR_OK  <br/> |0x00010000  <br/> |
|UPR_COMMIT  <br/> |0x00020000  <br/> |
|UPS_UPLOAD_ONLY  <br/> |0x00000001  <br/> |
|UPS_DNLOAD_ONLY  <br/> |0x00000002  <br/> |
|UPS_ONE_FOLDER  <br/> |0x00000004  <br/> |
|UPS_THESE_FOLDERS  <br/> |0x00000080  <br/> |
|UPS_OK  <br/> |0x00010000  <br/> |
|UPT_OK  <br/> |0x00010000  <br/> |
|UPT_PUBLIC  <br/> |0x00000001  <br/> |
|UPV_ERROR  <br/> |0x00010000  <br/> |
|UPV_DIRTY  <br/> |0x00020000  <br/> |
|UPV_COMMIT  <br/> |0x00040000  <br/> |
   
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

Use los dos siguientes identificadores de interfaz con [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), o [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir e ignorar cualquier comprobación de proveedor en un objeto de carpeta y un objeto de mensaje, respectivamente. 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a>Almacén de MAPI

Esta sección contiene las definiciones de constantes y los identificadores de interfaz utilizados por API que interactúan con un almacén MAPI.
  
### <a name="constants"></a>Constantes

||||
|:-----|:-----|:-----|
|fnevIndexing  <br/> |((ULONG) 0x00010000)  <br/> |Un proveedor de almacén puede especificar **fnevIndexing** en el miembro **ulEventType** de la estructura **[NOTIFICATION](notification.md)** para notificar al indizador que un objeto está listo para su indexación. El miembro **información** de la estructura **notificación** contiene una estructura ** [EXTENDED_NOTIFICATION](extended_notification.md)**.  <br/> |
|FS_NONE  <br/> |0x00  <br/> |Un cliente puede llamar a **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** y buscar la máscara de bits devuelta. **FS_NONE** indica que la carpeta no admite el uso compartido.  <br/> |
|FS_SUPPORTS_SHARING  <br/> |0x01  <br/> |Un cliente puede llamar a **IFolderSupport::GetSupportMask** y buscar la máscara de bits devuelta. **FS_SUPPORTS_SHARING** indica que la carpeta admite el uso compartido.  <br/> |
|INDEXING_SEARCH_OWNER  <br/> |((ULONG) 0x00000001)  <br/> |Identifica el proceso que está enviando una notificación a un indizador de que un objeto está listo para su indexación.  <br/> |
|MNID_ID  <br/> |Según se define en el archivo de encabezado winerror.h del Kit de desarrollo de Software (SDK) de Microsoft Windows  <br/> |Un valor para el campo **ulKind** de la estructura **[MAPINAMEID](mapinameid.md)**.  <br/> |
|MNID_STRING  <br/> |Según se define en el archivo de encabezado winerror.h del Kit de desarrollo de Software (SDK) de Microsoft Windows.  <br/> |Un valor para el campo **ulKind** de la estructura **[MAPINAMEID](mapinameid.md)**.  <br/> |
|MSCAP_RES_ANNOTATION  <br/> |((ULONG) 0x00000001)  <br/> |Si un cliente especifica **MSCAP_SEL_RESTRICTION** en *mscapSelector* para ** [IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** puede devolver este valor si el almacén ignora los parámetros no válidos en una restricción.  <br/> |
|MSCAP_SECURE_FOLDER_HOMEPAGES  <br/> |((ULONG) 0x00000020)  <br/> |Si un cliente especifica **MSCAP_SEL_FOLDER** en *mscapSelector* para **IMSCapabilities::GetCapabilities**, **GetCapabilities** puede devolver este valor si el almacén es un almacén no predeterminado que admite páginas principales de carpeta.  <br/> |
|STORE_PUSHER_OK  <br/> |((ULONG) 0x00800000)  <br/> |Un cliente puede obtener la propiedad ** [PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) ** para determinar la característica de un almacén de mensajes. Si el proveedor del almacén establece la marca **STORE_PUSHER_OK** en la máscara de bits, significa que el controlador de protocolo MAPI no rastreará el almacén, y el almacén es responsable de enviar cualquier cambio a través de notificaciones al indizador para que los mensajes sean indexados.  <br/> |
   
### <a name="definitions-for-namespaces"></a>Definiciones de espacios de nombres

Los siguientes identificadores únicos globales (GUID) representan los espacios de nombres de las propiedades con nombre. Están indexados por el controlador de protocolo (PH) MAPI y se documentan como de solo lectura.
  
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

Use la macro `DEFINE_OLEGUID` definida en el archivo de encabezado guiddef.h de Windows SDK para asociar el siguiente nombre simbólico GUID con su valor. 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a>Constantes de libreta de direcciones MAPI

Esta sección contiene las definiciones de constantes de la libreta de direcciones MAPI.
  
### <a name="constants"></a>Constantes

||||
|:-----|:-----|:-----|
|CONTAB_ROOT  <br/> |((ULONG) 0x00000001)  <br/> |La carpeta raíz de un objeto de libreta de direcciones MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |((ULONG) 0x00000002)  <br/> |Una subcarpeta incluida en la carpeta raíz del objeto de la libreta de direcciones MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |((ULONG) 0x00000003)  <br/> |Un objeto contenedor de libreta de direcciones.  <br/> |
|CONTAB_USER  <br/> |((ULONG) 0x00000004)  <br/> |Un objeto de usuario de mensajería.  <br/> |
|CONTAB_DISTLIST  <br/> |((ULONG) 0x00000005)  <br/> |Un objeto de la lista de distribución.  <br/> |
   
## <a name="additional-mapi-constants"></a>Constantes MAPI adicionales

Esta sección contiene las definiciones de constantes que incluyen códigos de error y los identificadores de interfaz usados por la API de MAPI que no se han expuesto y documentado previamente.
  
||||
|:-----|:-----|:-----|
|DIALOG_MODAL  <br/> |((ULONG) 0x00000001)  <br/> |Cuando un cliente llama al método [IAddrBook::Details](iaddrbook-details.md), el cliente debe configurar la marca **DIALOG_MODAL** en el parámetro _ulFlags_ parámetro para mostrar el cuadro de diálogo modal con los detalles sobre una entrada de la libreta de direcciones determinada. Esta constante se define en mapidefs.h.  <br/> |
|ITEMPROC_FORCE  <br/> |0x00000800  <br/> |En Outlook 2007, los almacenes de archivos PST ajustados procesan los nuevos mensajes con filtros de spam y reglas antes de que se notifique a los clientes de MAPI de los mensajes nuevos. .Un proveedor o un cliente que use el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)  para crear un nuevo mensaje en los almacenes PST debe establecer la marca **ITEMPROC_FORCE** en el parámetro _ulFlags_ del método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para indicar al almacén de archivos PST que el mensaje es apto para el procesamiento de reglas antes de que el almacén notifique a cualquier cliente en escucha de la llegada del nuevo mensaje. Tenga en cuenta que dichas reglas de procesamiento solo se aplican a los nuevos mensajes creados en un servidor que no sea un Microsoft Exchange Server, ya que Exchange Server procesa las reglas para los mensajes en el servidor. Por lo tanto, el proveedor o cliente que crea un mensaje debe pasar este indicador junto con **NON_EMS_XP_SAVE**, lo que indica que el servidor no es un servidor de Exchange.  <br/> |
| MAPI_BG_SESSION  <br/> |0x00200000  <br/> |Un cliente puede llamar a la función [MAPILogonEx](mapilogonex.md), configurando la marca **MAPI_BG_SESSION** en el parámetro _flFlags_ para iniciar una sesión y llevar a cabo cualquier operación en segundo plano. En general, si un cliente pretende realizar procesamiento en un subproceso en segundo plano o en un proceso independiente de manera que no altere el subproceso de primer plano, debe llamar a [MAPILogonEx](mapilogonex.md) con la marca **MAPI_BG_SESSION**. Un ejemplo en el que se utiliza es una aplicación de cliente, como un motor de indexación, que abre un archivo de carpetas personales (PST) para un acceso de fondo.  <br/> |
|MAPI_CACHE_ONLY  <br/> |0x00004000  <br/> |Un cliente puede llamar al método [IAddrBook::OpenEntry](iaddrbook-openentry.md), estableciendo la marca **MAPI_CACHE_ONLY** en el parámetro _ulFlags_ para abrir una entrada de la libreta de direcciones y posteriormente obtener acceso a ella solo desde la caché. Un ejemplo en el que se utiliza es una aplicación de cliente que quiere abrir la lista global de direcciones en el modo caché de Exchange y obtener acceso a una entrada de esa libreta de direcciones de la memoria caché sin crear tráfico entre el cliente y el servidor.  <br/> |
|MAPI_DIALOG_MODELESS  <br/> |0x0000000C  <br/> |Este valor puede pasarse a la función MAPISendMail de Simple MAPI en el parámetro _ulFlags_ para especificar que se muestra un cuadro de diálogo sin modo mediante la aplicación de correo predeterminada. Si no se establecen ni este indicador ni MAPI_DIALOG (0 x 00000008), no se mostrará ningún cuadro de diálogo.  <br/> |
|MAPI_NO_CACHE  <br/> |0x00000200  <br/> |Si Microsoft Office Outlook está en modo caché de Exchange y se ha abierto un almacén en modo caché, un cliente o proveedor de servicios puede llamar a [IMsgStore::OpenEntry](imsgstore-openentry.md), estableciendo la marca **MAPI_NO_CACHE** en el parámetro _ulFlags_ para abrir un elemento o una carpeta en el almacén remoto. Tenga en cuenta que, si abre el almacén de mensajes con la marca **MDB_ONLINE** en el servidor remoto, no tiene que usar la marca **MAPI_NO_CACHE**.  <br/> |
|MAPI_UNICODE  <br/> |0x80000000  <br/> |Un cliente o proveedor de servicios puede llamar a la función [OpenIMsgOnIStg](openimsgonistg.md), configurando la marca **MAPI_UNICODE** en el parámetro _ulFlags_ para crear archivos .msg Unicode. El archivo [IMessage: IMAPIProp](imessageimapiprop.md) resultante muestra **STORE_UNICODE_OK** en su [Propiedad canónica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) y es compatible con propiedades Unicode. Esta constante se define en mapidefs.h.  <br/> |
|MDB_ONLINE  <br/> |0x00000100  <br/> |Si Outlook está en  modo caché de Exchange, un cliente o proveedor de servicios puede llamar al método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), estableciendo la marca **MDB_ONLINE** en el parámetro _ulFlags_ para invalidar la conexión con el almacén de mensajes locales y abrir el almacén en el servidor remoto. Tenga en cuenta que no puede abrir un almacén de Exchange en el modo caché y en modo sin caché al mismo tiempo en la misma sesión MAPI. Si ya ha abierto el almacén de mensajes en modo caché, debe cerrar el almacén antes de abrirlo con esta marca o abrir una nueva sesión MAPI donde puede abrir el almacén de Exchange en el servidor remoto mediante este marcador.  <br/> |
|NON_EMS_XP_SAVE  <br/> |0x00001000  <br/> |Un cliente puede llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md), estableciendo la marca **NON_EMS_XP_SAVE** en el parámetro _ulFlags_ para indicar que el mensaje no se ha entregado desde un servidor de Exchange. Esta marca puede usarse junto con la marca **ITEMPROC_FORCE** en el parámetro _ulFlags_ para indicar a un almacén PST que el mensaje es apto para el procesamiento de reglas antes de que el almacén PST notifique  a cualquier cliente en escucha de la llegada del mensaje. Esto reglas de procesamiento solo se aplican a los nuevos mensajes creados con [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en un servidor que no es un servidor de Exchange (en cuyo caso el servidor Exchange ya habría procesado reglas en el mensaje).  <br/> |
|SPAMFILTER_ONSAVE  <br/> |0x00000080  <br/> |Un cliente puede llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md), estableciendo la marca **SPAMFILTER_ONSAVE** en el parámetro _ulFlags_ para habilitar el filtrado de spam en un mensaje que se está guardando. El soporte de filtrado de spam solo está disponible si el tipo de dirección de correo electrónico del remitente es Protocolo simple de transferencia de correo (SMTP) y el mensaje se está guardando en un almacén de un archivo de carpetas personales (PST).  <br/> |
|STORE_ITEMPROC  <br/> |0x00200000  <br/> |Si se establece esta marca en la [Propiedad canónica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) de un almacén de archivos PST ajustado, indica que cuando llega un mensaje nuevo al almacén, el almacén procesa reglas y filtrado antispam del mensaje por separado. A continuación el almacén llama a [IMAPISupport::Notify](imapisupport-notify.md), configurando **fnevNewMail** en la estructura [notificación](notification.md) estructura que se pasa como un parámetro y pasando los detalles del nuevo mensaje a un cliente en escucha. Posteriormente, cuando el cliente en escucha recibe la notificación, no procesa las reglas en el mensaje.  <br/> |
|STORE_UNICODE_OK  <br/> |0x00040000  <br/> |Si esta marca se incluye en la [Propiedad canónica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), indica que el almacén admite almacenamiento Unicode. Un cliente puede buscar la presencia de la marca para decidir si desea solicitar o guardar información Unicode en el almacén.  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a>Definiciones para archivar elementos en una carpeta

Las siguientes definiciones de constantes son valores que se usan para configurar la [Propiedad canónica PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a>Definiciones para mostrar objetos remotos

Las definiciones de macros y constantes siguientes son para mostrar los objetos remotos. Para obtener más información, vea la [Propiedad canónica PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a>Definiciones de libreta de direcciones de Exchange y códigos de error del almacén de mensajes

A continuación se muestran las definiciones de códigos de error de la libreta de direcciones de Exchange y el almacén de mensajes, que tienen capacidad de reconexión. La última llamada a un catálogo global (GC) desconectado puede dar como resultado el error **MAPI_E_END_OF_SESSION**, que debería volverse a intentar. 
  
MAPI de Outlook es compatible con la reconexión a un servidor de catálogo global sin reconfiguración especial, pero puede que se devuelvan otros códigos de error al cliente.
  
||||
|:-----|:-----|:-----|
|MAPI_E_END_OF_SESSION  <br/> |0x80040200  <br/> |Se devuelve cuando se ha desconectado una conexión.  <br/> |
|MAPI_E_RECONNECTED  <br/> |0x80040125  <br/> |Se devuelve cuando el token de conexión de llamada a procedimiento remoto (RPC) no está actualizado. Si el token de la transacción actual es diferente del token de la conexión, significa que se ha vuelto a conectar, por lo que se devuelve **MAPI_E_RECONNECTED** y se puede tratar del mismo modo que **MAPI_E_END_OF_SESSION**. Debería volver a intentar la llamada.  <br/> |
|MAPI_E_OFFLINE  <br/> |0x80040126  <br/> |Se devuelve cuando la conexión está desconectada. Normalmente, esto significa que ha ocurrido algo en el entorno, como errores en el servidor o pérdida de conectividad de red. Es más probable que aparezca este error al usar el modo caché de un perfil e intenta evitar la caché para comunicarse con el servidor. Si la caché no pudo inicialmente establecer una conexión con el servidor, puede que esté en el estado sin conexión en el que **MAPI_E_OFFLINE** puede aparecer.  <br/> |
   
Ninguno de los dos errores anteriores se devolverán en todos los escenarios donde parece probable que se aplicasen. En la mayoría de los casos, se devolverán **MAPI\_E_NETWORK_ERROR** o **MAPI_E_CALL_FAILED**. Ninguno aparecerá al usar la descarga de [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440). 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a>Definiciones para las cuotas del modo de almacenamiento en caché del buzón de correo Exchange Server

Las siguientes definiciones de constantes son usadas por Microsoft Outlook 2010 y Microsoft Outlook 2013 para configurar las cuotas del perfil en modo caché de Exchange que son equivalentes a las cuotas de buzón de Exchange que, en caso contrario, sólo están disponibles con un perfil en línea.
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

Estas propiedades se asignan a sus propiedades en línea correspondientes y contienen los mismos valores en kilobytes. PR_QUOTA_WARNING se asigna a PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND a PR_QUOTA_PROHIBIT_SEND_QUOTA y PR_QUOTA_RECEIVE a PR_PROHIBIT_RECEIVE_QUOTA.
  
### <a name="definitions-for-message-format"></a>Definiciones de formato del mensaje

Las siguientes definiciones de constantes son valores que se usan para configurar la [Propiedad canónica PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a>Definiciones para usar RPC a través de HTTP

Consulte el tema [Propiedad canónica PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) para obtener definiciones de constantes usadas como marcas para establecer la propiedad. 
  
Consulte el tema [Propiedad canónica PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) para obtener definiciones de constantes usadas para establecer la propiedad. 
  
### <a name="identifiers"></a>Identificadores

Use la macro `DEFINE_OLEGUID` definida en el archivo de encabezado guiddef.h del Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar los siguientes nombres simbólicos GUID a sus valores. 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

El siguiente identificador es para la sección de perfil Capone de una libreta de direcciones, que como apoyo a buzones múltiples de Exchange ([MultiEx](using-multiple-exchange-accounts.md)) contiene una propiedad [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) que desactiva de forma efectiva el contenedor predeterminado especificado por [SetDefaultDir](iaddrbook-setdefaultdir.md).
  
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

### <a name="pst-override-handler-interface-identifiers"></a>Identificadores de interfaz del controlador de invalidación PST

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

## <a name="see-also"></a>Vea también

- [Acerca de las adiciones de MAPI](about-mapi-additions.md) 
- [Acerca de las propiedades con nombre que usa Outlook](about-named-properties-used-by-outlook.md)
- [Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Administrar un mensaje en un OST sin invocar una sincronización en el modo de intercambio en caché](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

