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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318924"
---
# <a name="mapi-constants"></a><span data-ttu-id="74212-103">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="74212-103">MAPI constants</span></span>

<span data-ttu-id="74212-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74212-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74212-105">Este tema contiene las definiciones de constantes, declaraciones de interfaz MAPI e identificadores de clase e interfaz usados por las API de MAPI.</span><span class="sxs-lookup"><span data-stu-id="74212-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="74212-106">Identificadores de clase e interfaz</span><span class="sxs-lookup"><span data-stu-id="74212-106">Class and interface identifiers</span></span>

<span data-ttu-id="74212-107">Use la macro DEFINE_GUID definida en el archivo de encabezado guiddef.h del Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar nombres simbólicos de identificador único global (GUID) con sus valores, a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="74212-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="74212-108">API de conversión de seguridad de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="74212-108">Attachment security conversion API</span></span>

<span data-ttu-id="74212-109">Esta sección contiene las definiciones de constantes e identificadores de interfaz de la API de seguridad de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="74212-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="74212-110">Utilice la macro MAPIMETHOD definida en el archivo de encabezado mapidefs.h de Windows SDK para definir la función virtual pura **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span><span class="sxs-lookup"><span data-stu-id="74212-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="74212-111">Utilice la macro DECLARE_MAPI_INTERFACE_ definida en el archivo de encabezado mapidefs.h de Windows SDK para definir la tabla de método virtual de \*\* [IAttachmentSecurity](iattachmentsecurityiunknown.md)\*\*.</span><span class="sxs-lookup"><span data-stu-id="74212-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="74212-112">API de conversión de MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="74212-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="74212-113">Esta sección contiene las definiciones de constantes e identificadores de clase e interfaz para la API de conversión de MAPI-MIME.</span><span class="sxs-lookup"><span data-stu-id="74212-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="74212-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="74212-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74212-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="74212-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="74212-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="74212-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="74212-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="74212-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="74212-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="74212-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="74212-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="74212-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="74212-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="74212-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="74212-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="74212-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="74212-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="74212-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="74212-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="74212-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="74212-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="74212-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="74212-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="74212-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="74212-126">0x0080</span><span class="sxs-lookup"><span data-stu-id="74212-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="74212-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="74212-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="74212-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="74212-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="74212-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="74212-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="74212-130">0x4000</span><span class="sxs-lookup"><span data-stu-id="74212-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="74212-131">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="74212-131">CCSF_GLOBAL_MESSAGE</span></span>  <br/> |<span data-ttu-id="74212-132">0x00200000</span><span class="sxs-lookup"><span data-stu-id="74212-132">0x00200000</span></span>  <br/> |
|<span data-ttu-id="74212-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="74212-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="74212-134">*Según se define en el archivo de encabezado winerror.h del Kit de desarrollo de Software (SDK) de Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="74212-134">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="74212-135">Identificadores de clase</span><span class="sxs-lookup"><span data-stu-id="74212-135">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="74212-136">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="74212-136">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="74212-137">API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="74212-137">Offline State API</span></span>

<span data-ttu-id="74212-138">Esta sección contiene las definiciones de constantes e identificadores de clase e interfaz para la API de estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="74212-138">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="74212-139">Constantes</span><span class="sxs-lookup"><span data-stu-id="74212-139">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74212-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="74212-140">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="74212-141">*Según se define en el archivo de encabezado winerror.h del Kit de desarrollo de Software (SDK) de Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="74212-141">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="74212-142">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="74212-142">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="74212-143">*Según se define en el archivo de encabezado winerror.h de Windows (SDK) de Windows*</span><span class="sxs-lookup"><span data-stu-id="74212-143">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="74212-144">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="74212-144">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="74212-145">(ULONG)0</span><span class="sxs-lookup"><span data-stu-id="74212-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="74212-146">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="74212-146">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="74212-147">(ULONG)0</span><span class="sxs-lookup"><span data-stu-id="74212-147">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="74212-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="74212-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="74212-149">1</span><span class="sxs-lookup"><span data-stu-id="74212-149">1</span></span>  <br/> |
|<span data-ttu-id="74212-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="74212-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="74212-151">0x1</span><span class="sxs-lookup"><span data-stu-id="74212-151">0x1</span></span>  <br/> |
|<span data-ttu-id="74212-152">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="74212-152">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="74212-153">0x2</span><span class="sxs-lookup"><span data-stu-id="74212-153">0x2</span></span>  <br/> |
|<span data-ttu-id="74212-154">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="74212-154">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="74212-155">0x00002000</span><span class="sxs-lookup"><span data-stu-id="74212-155">0x00002000</span></span>  <br/> |
|<span data-ttu-id="74212-156">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="74212-156">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="74212-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74212-157">0x00000000</span></span>  <br/> |
|<span data-ttu-id="74212-158">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="74212-158">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="74212-159">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="74212-159">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="74212-160">**En línea o sin conexión**</span><span class="sxs-lookup"><span data-stu-id="74212-160">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="74212-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="74212-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="74212-162">0x00000003</span><span class="sxs-lookup"><span data-stu-id="74212-162">0x00000003</span></span>  <br/> |
|<span data-ttu-id="74212-163">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="74212-163">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="74212-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="74212-164">0x00000001</span></span>  <br/> |
|<span data-ttu-id="74212-165">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="74212-165">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="74212-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="74212-166">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="74212-167">Identificadores de clase</span><span class="sxs-lookup"><span data-stu-id="74212-167">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="74212-168">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="74212-168">Interface identifiers</span></span>

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

## <a name="outlook-named-properties"></a><span data-ttu-id="74212-169">Propiedades con nombre de Outlook</span><span class="sxs-lookup"><span data-stu-id="74212-169">Outlook named properties</span></span>

<span data-ttu-id="74212-170">Esta sección contiene las definiciones de constantes de propiedades con nombre, sus espacios de nombres y otras constantes relacionadas.</span><span class="sxs-lookup"><span data-stu-id="74212-170">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="74212-171">Definiciones de propiedades con nombre</span><span class="sxs-lookup"><span data-stu-id="74212-171">Definitions for named properties</span></span>

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

### <a name="definitions-for-namespaces"></a><span data-ttu-id="74212-172">Definiciones de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="74212-172">Definitions for namespaces</span></span>

<span data-ttu-id="74212-173">Los siguientes identificadores únicos globales (GUID) representan los espacios de nombres de las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="74212-173">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
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

<span data-ttu-id="74212-174">Consulte la sección del almacén de MAPI para las definiciones de PSETID.</span><span class="sxs-lookup"><span data-stu-id="74212-174">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="74212-175">Otras constantes</span><span class="sxs-lookup"><span data-stu-id="74212-175">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74212-176">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="74212-176">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="74212-177">0xD000000</span><span class="sxs-lookup"><span data-stu-id="74212-177">0xD000000</span></span>  <br/> |
|<span data-ttu-id="74212-178">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="74212-178">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="74212-179">0x2000000</span><span class="sxs-lookup"><span data-stu-id="74212-179">0x2000000</span></span>  <br/> |
|<span data-ttu-id="74212-180">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="74212-180">MNID_ID</span></span>  <br/> | <span data-ttu-id="74212-181">*Según se define en el archivo de encabezadomapidefs.h.*</span><span class="sxs-lookup"><span data-stu-id="74212-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="74212-182">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="74212-182">MNID_STRING</span></span>  <br/> | <span data-ttu-id="74212-183">*Según se define en el archivo de encabezadomapidefs.h.*</span><span class="sxs-lookup"><span data-stu-id="74212-183">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="74212-184">mtgNone</span><span class="sxs-lookup"><span data-stu-id="74212-184">mtgNone</span></span>  <br/> |<span data-ttu-id="74212-185">0x0</span><span class="sxs-lookup"><span data-stu-id="74212-185">0x0</span></span>  <br/> |
|<span data-ttu-id="74212-186">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="74212-186">mtgRequest</span></span>  <br/> |<span data-ttu-id="74212-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="74212-187">0x00000001</span></span>  <br/> |
|<span data-ttu-id="74212-188">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="74212-188">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="74212-189">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-189">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-190">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="74212-190">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="74212-191">0x00020000</span><span class="sxs-lookup"><span data-stu-id="74212-191">0x00020000</span></span>  <br/> |
|<span data-ttu-id="74212-192">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="74212-192">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="74212-193">0x00080000</span><span class="sxs-lookup"><span data-stu-id="74212-193">0x00080000</span></span>  <br/> |
|<span data-ttu-id="74212-194">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="74212-194">mtgDelegated</span></span>  <br/> |<span data-ttu-id="74212-195">0x00100000</span><span class="sxs-lookup"><span data-stu-id="74212-195">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="74212-196">API de replicación</span><span class="sxs-lookup"><span data-stu-id="74212-196">Replication API</span></span>

<span data-ttu-id="74212-197">Esta sección contiene las definiciones de constantes, declaraciones de interfaz MAPI e identificadores de clase e interfaz de la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="74212-197">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="74212-198">Constantes</span><span class="sxs-lookup"><span data-stu-id="74212-198">Constants</span></span>

<span data-ttu-id="74212-199">Esta es una estructura [MAPIUID](mapiuid.md) que identifica un proveedor de servicios MAPI:</span><span class="sxs-lookup"><span data-stu-id="74212-199">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="74212-200">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="74212-200">DNH_OK</span></span>  <br/> |<span data-ttu-id="74212-201">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-202">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="74212-202">DNT_OK</span></span>  <br/> |<span data-ttu-id="74212-203">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-203">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-204">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="74212-204">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="74212-205">0x00000008</span><span class="sxs-lookup"><span data-stu-id="74212-205">0x00000008</span></span>  <br/> |
|<span data-ttu-id="74212-206">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="74212-206">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="74212-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74212-207">0x00000010</span></span>  <br/> |
|<span data-ttu-id="74212-208">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="74212-208">HSF_OK</span></span>  <br/> |<span data-ttu-id="74212-209">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-209">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-210">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="74212-210">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="74212-211">((ULONG) 0x00000800)</span><span class="sxs-lookup"><span data-stu-id="74212-211">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="74212-212">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="74212-212">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="74212-213">((ULONG) 0x00001000)</span><span class="sxs-lookup"><span data-stu-id="74212-213">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="74212-214">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="74212-214">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="74212-215">((ULONG) 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="74212-215">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="74212-216">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="74212-216">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="74212-217">comprendi</span><span class="sxs-lookup"><span data-stu-id="74212-217">0</span></span>  <br/> |
|<span data-ttu-id="74212-218">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="74212-218">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="74212-219">1</span><span class="sxs-lookup"><span data-stu-id="74212-219">1</span></span>  <br/> |
|<span data-ttu-id="74212-220">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="74212-220">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="74212-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="74212-221">0x00000001</span></span>  <br/> |
|<span data-ttu-id="74212-222">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="74212-222">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="74212-223">0x00000002</span><span class="sxs-lookup"><span data-stu-id="74212-223">0x00000002</span></span>  <br/> |
|<span data-ttu-id="74212-224">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="74212-224">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="74212-225">0x00000040</span><span class="sxs-lookup"><span data-stu-id="74212-225">0x00000040</span></span>  <br/> |
|<span data-ttu-id="74212-226">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="74212-226">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="74212-227">0x00000080</span><span class="sxs-lookup"><span data-stu-id="74212-227">0x00000080</span></span>  <br/> |
|<span data-ttu-id="74212-228">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="74212-228">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="74212-229">0x00000200</span><span class="sxs-lookup"><span data-stu-id="74212-229">0x00000200</span></span>  <br/> |
|<span data-ttu-id="74212-230">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="74212-230">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="74212-231">0x00001000</span><span class="sxs-lookup"><span data-stu-id="74212-231">0x00001000</span></span>  <br/> |
|<span data-ttu-id="74212-232">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="74212-232">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="74212-233">0x00020000</span><span class="sxs-lookup"><span data-stu-id="74212-233">0x00020000</span></span>  <br/> |
|<span data-ttu-id="74212-234">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="74212-234">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="74212-235">0x02000000</span><span class="sxs-lookup"><span data-stu-id="74212-235">0x02000000</span></span>  <br/> |
|<span data-ttu-id="74212-236">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="74212-236">UPC_OK</span></span>  <br/> |<span data-ttu-id="74212-237">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-237">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-238">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="74212-238">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="74212-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="74212-239">0x00000001</span></span>  <br/> |
|<span data-ttu-id="74212-240">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="74212-240">UPD_MOV</span></span>  <br/> |<span data-ttu-id="74212-241">0x00000002</span><span class="sxs-lookup"><span data-stu-id="74212-241">0x00000002</span></span>  <br/> |
|<span data-ttu-id="74212-242">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="74212-242">UPD_OK</span></span>  <br/> |<span data-ttu-id="74212-243">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-243">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-244">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="74212-244">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="74212-245">0x00020000</span><span class="sxs-lookup"><span data-stu-id="74212-245">0x00020000</span></span>  <br/> |
|<span data-ttu-id="74212-246">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="74212-246">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="74212-247">0x00040000</span><span class="sxs-lookup"><span data-stu-id="74212-247">0x00040000</span></span>  <br/> |
|<span data-ttu-id="74212-248">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="74212-248">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="74212-249">0x00080000</span><span class="sxs-lookup"><span data-stu-id="74212-249">0x00080000</span></span>  <br/> |
|<span data-ttu-id="74212-250">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="74212-250">UPF_NEW</span></span>  <br/> |<span data-ttu-id="74212-251">0x00000001</span><span class="sxs-lookup"><span data-stu-id="74212-251">0x00000001</span></span>  <br/> |
|<span data-ttu-id="74212-252">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="74212-252">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="74212-253">0x00000002</span><span class="sxs-lookup"><span data-stu-id="74212-253">0x00000002</span></span>  <br/> |
|<span data-ttu-id="74212-254">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="74212-254">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="74212-255">0x00000004</span><span class="sxs-lookup"><span data-stu-id="74212-255">0x00000004</span></span>  <br/> |
|<span data-ttu-id="74212-256">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="74212-256">UPF_DEL</span></span>  <br/> |<span data-ttu-id="74212-257">0x00000008</span><span class="sxs-lookup"><span data-stu-id="74212-257">0x00000008</span></span>  <br/> |
|<span data-ttu-id="74212-258">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="74212-258">UPF_OK</span></span>  <br/> |<span data-ttu-id="74212-259">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-260">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="74212-260">UPH_OK</span></span>  <br/> |<span data-ttu-id="74212-261">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-261">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-262">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="74212-262">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="74212-263">0x00000001</span><span class="sxs-lookup"><span data-stu-id="74212-263">0x00000001</span></span>  <br/> |
|<span data-ttu-id="74212-264">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="74212-264">UPM_NEW</span></span>  <br/> |<span data-ttu-id="74212-265">0x00000002</span><span class="sxs-lookup"><span data-stu-id="74212-265">0x00000002</span></span>  <br/> |
|<span data-ttu-id="74212-266">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="74212-266">UPM_MOV</span></span>  <br/> |<span data-ttu-id="74212-267">0x00000004</span><span class="sxs-lookup"><span data-stu-id="74212-267">0x00000004</span></span>  <br/> |
|<span data-ttu-id="74212-268">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="74212-268">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="74212-269">0x00000008</span><span class="sxs-lookup"><span data-stu-id="74212-269">0x00000008</span></span>  <br/> |
|<span data-ttu-id="74212-270">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="74212-270">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="74212-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74212-271">0x00000010</span></span>  <br/> |
|<span data-ttu-id="74212-272">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="74212-272">UPM_OK</span></span>  <br/> |<span data-ttu-id="74212-273">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-273">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-274">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="74212-274">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="74212-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="74212-275">0x00020000</span></span>  <br/> |
|<span data-ttu-id="74212-276">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="74212-276">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="74212-277">0x00040000</span><span class="sxs-lookup"><span data-stu-id="74212-277">0x00040000</span></span>  <br/> |
|<span data-ttu-id="74212-278">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="74212-278">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="74212-279">0x00080000</span><span class="sxs-lookup"><span data-stu-id="74212-279">0x00080000</span></span>  <br/> |
|<span data-ttu-id="74212-280">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="74212-280">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="74212-281">0x00100000</span><span class="sxs-lookup"><span data-stu-id="74212-281">0x00100000</span></span>  <br/> |
|<span data-ttu-id="74212-282">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="74212-282">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="74212-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="74212-283">0x00000001</span></span>  <br/> |
|<span data-ttu-id="74212-284">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="74212-284">UPR_READ</span></span>  <br/> |<span data-ttu-id="74212-285">0x00000002</span><span class="sxs-lookup"><span data-stu-id="74212-285">0x00000002</span></span>  <br/> |
|<span data-ttu-id="74212-286">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="74212-286">UPR_OK</span></span>  <br/> |<span data-ttu-id="74212-287">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-287">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-288">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="74212-288">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="74212-289">0x00020000</span><span class="sxs-lookup"><span data-stu-id="74212-289">0x00020000</span></span>  <br/> |
|<span data-ttu-id="74212-290">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="74212-290">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="74212-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="74212-291">0x00000001</span></span>  <br/> |
|<span data-ttu-id="74212-292">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="74212-292">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="74212-293">0x00000002</span><span class="sxs-lookup"><span data-stu-id="74212-293">0x00000002</span></span>  <br/> |
|<span data-ttu-id="74212-294">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="74212-294">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="74212-295">0x00000004</span><span class="sxs-lookup"><span data-stu-id="74212-295">0x00000004</span></span>  <br/> |
|<span data-ttu-id="74212-296">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="74212-296">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="74212-297">0x00000080</span><span class="sxs-lookup"><span data-stu-id="74212-297">0x00000080</span></span>  <br/> |
|<span data-ttu-id="74212-298">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="74212-298">UPS_OK</span></span>  <br/> |<span data-ttu-id="74212-299">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-300">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="74212-300">UPT_OK</span></span>  <br/> |<span data-ttu-id="74212-301">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-301">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-302">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="74212-302">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="74212-303">0x00000001</span><span class="sxs-lookup"><span data-stu-id="74212-303">0x00000001</span></span>  <br/> |
|<span data-ttu-id="74212-304">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="74212-304">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="74212-305">0x00010000</span><span class="sxs-lookup"><span data-stu-id="74212-305">0x00010000</span></span>  <br/> |
|<span data-ttu-id="74212-306">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="74212-306">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="74212-307">0x00020000</span><span class="sxs-lookup"><span data-stu-id="74212-307">0x00020000</span></span>  <br/> |
|<span data-ttu-id="74212-308">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="74212-308">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="74212-309">0x00040000</span><span class="sxs-lookup"><span data-stu-id="74212-309">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="74212-310">Declaraciones de interfaz</span><span class="sxs-lookup"><span data-stu-id="74212-310">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="74212-311">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="74212-311">Interface identifiers</span></span>

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

<span data-ttu-id="74212-312">Use los dos siguientes identificadores de interfaz con [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), o [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir e ignorar cualquier comprobación de proveedor en un objeto de carpeta y un objeto de mensaje, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="74212-312">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="74212-313">Almacén de MAPI</span><span class="sxs-lookup"><span data-stu-id="74212-313">MAPI store</span></span>

<span data-ttu-id="74212-314">Esta sección contiene las definiciones de constantes y los identificadores de interfaz utilizados por API que interactúan con un almacén MAPI.</span><span class="sxs-lookup"><span data-stu-id="74212-314">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="74212-315">Constantes</span><span class="sxs-lookup"><span data-stu-id="74212-315">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="74212-316">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="74212-316">fnevIndexing</span></span>  <br/> |<span data-ttu-id="74212-317">((ULONG) 0x00010000)</span><span class="sxs-lookup"><span data-stu-id="74212-317">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="74212-318">Un proveedor de almacén puede especificar **fnevIndexing** en el miembro **ulEventType** de la estructura **[NOTIFICATION](notification.md)** para notificar al indizador que un objeto está listo para su indexación.</span><span class="sxs-lookup"><span data-stu-id="74212-318">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="74212-319">El miembro **información** de la estructura **notificación** contiene una estructura \*\* [EXTENDED_NOTIFICATION](extended_notification.md)\*\*.</span><span class="sxs-lookup"><span data-stu-id="74212-319">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="74212-320">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="74212-320">FS_NONE</span></span>  <br/> |<span data-ttu-id="74212-321">0x00</span><span class="sxs-lookup"><span data-stu-id="74212-321">0x00</span></span>  <br/> |<span data-ttu-id="74212-322">Un cliente puede llamar a **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** y buscar la máscara de bits devuelta.</span><span class="sxs-lookup"><span data-stu-id="74212-322">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="74212-323">**FS_NONE** indica que la carpeta no admite el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="74212-323">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="74212-324">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="74212-324">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="74212-325">0x01</span><span class="sxs-lookup"><span data-stu-id="74212-325">0x01</span></span>  <br/> |<span data-ttu-id="74212-326">Un cliente puede llamar a **IFolderSupport::GetSupportMask** y buscar la máscara de bits devuelta.</span><span class="sxs-lookup"><span data-stu-id="74212-326">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="74212-327">**FS_SUPPORTS_SHARING** indica que la carpeta admite el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="74212-327">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="74212-328">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="74212-328">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="74212-329">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="74212-329">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="74212-330">Identifica el proceso que está enviando una notificación a un indizador de que un objeto está listo para su indexación.</span><span class="sxs-lookup"><span data-stu-id="74212-330">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="74212-331">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="74212-331">MNID_ID</span></span>  <br/> |<span data-ttu-id="74212-332">Según se define en el archivo de encabezado winerror.h del Kit de desarrollo de Software (SDK) de Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="74212-332">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="74212-333">Un valor para el campo **ulKind** de la estructura **[MAPINAMEID](mapinameid.md)**.</span><span class="sxs-lookup"><span data-stu-id="74212-333">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="74212-334">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="74212-334">MNID_STRING</span></span>  <br/> |<span data-ttu-id="74212-335">Según se define en el archivo de encabezado winerror.h del Kit de desarrollo de Software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="74212-335">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="74212-336">Un valor para el campo **ulKind** de la estructura **[MAPINAMEID](mapinameid.md)**.</span><span class="sxs-lookup"><span data-stu-id="74212-336">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="74212-337">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="74212-337">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="74212-338">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="74212-338">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="74212-339">Si un cliente especifica **MSCAP_SEL_RESTRICTION** en *mscapSelector* para \*\* [IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)\*\*, **GetCapabilities** puede devolver este valor si el almacén ignora los parámetros no válidos en una restricción.</span><span class="sxs-lookup"><span data-stu-id="74212-339">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="74212-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="74212-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="74212-341">((ULONG) 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="74212-341">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="74212-342">Si un cliente especifica **MSCAP_SEL_FOLDER** en *mscapSelector* para **IMSCapabilities::GetCapabilities**, **GetCapabilities** puede devolver este valor si el almacén es un almacén no predeterminado que admite páginas principales de carpeta.</span><span class="sxs-lookup"><span data-stu-id="74212-342">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="74212-343">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="74212-343">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="74212-344">((ULONG) 0x00800000)</span><span class="sxs-lookup"><span data-stu-id="74212-344">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="74212-345">Un cliente puede obtener la propiedad \*\* [PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) \*\* para determinar la característica de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="74212-345">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="74212-346">Si el proveedor del almacén establece la marca **STORE_PUSHER_OK** en la máscara de bits, significa que el controlador de protocolo MAPI no rastreará el almacén, y el almacén es responsable de enviar cualquier cambio a través de notificaciones al indizador para que los mensajes sean indexados.</span><span class="sxs-lookup"><span data-stu-id="74212-346">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="74212-347">Definiciones de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="74212-347">Definitions for namespaces</span></span>

<span data-ttu-id="74212-348">Los siguientes identificadores únicos globales (GUID) representan los espacios de nombres de las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="74212-348">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="74212-349">Están indexados por el controlador de protocolo (PH) MAPI y se documentan como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="74212-349">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="74212-350">Las propiedades con nombre no deben usarse para crear o modificar elementos.</span><span class="sxs-lookup"><span data-stu-id="74212-350">The named properties should not be used to create or modify items.</span></span> 
  
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

#### <a name="mnidid-properties"></a><span data-ttu-id="74212-351">Propiedades MNID_ID</span><span class="sxs-lookup"><span data-stu-id="74212-351">MNID_ID Properties</span></span>
  
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

#### <a name="mnidstring-properties"></a><span data-ttu-id="74212-352">Propiedades MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="74212-352">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="74212-353">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="74212-353">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="74212-354">Use la macro `DEFINE_OLEGUID` definida en el archivo de encabezado guiddef.h de Windows SDK para asociar el siguiente nombre simbólico GUID con su valor.</span><span class="sxs-lookup"><span data-stu-id="74212-354">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="74212-355">Constantes de libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="74212-355">MAPI Address Book constants</span></span>

<span data-ttu-id="74212-356">Esta sección contiene las definiciones de constantes de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="74212-356">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="74212-357">Constantes</span><span class="sxs-lookup"><span data-stu-id="74212-357">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="74212-358">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="74212-358">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="74212-359">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="74212-359">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="74212-360">La carpeta raíz de un objeto de libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="74212-360">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="74212-361">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="74212-361">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="74212-362">((ULONG) 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="74212-362">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="74212-363">Una subcarpeta incluida en la carpeta raíz del objeto de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="74212-363">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="74212-364">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="74212-364">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="74212-365">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="74212-365">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="74212-366">Un objeto contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="74212-366">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="74212-367">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="74212-367">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="74212-368">((ULONG) 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="74212-368">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="74212-369">Un objeto de usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="74212-369">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="74212-370">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="74212-370">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="74212-371">((ULONG) 0x00000005)</span><span class="sxs-lookup"><span data-stu-id="74212-371">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="74212-372">Un objeto de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="74212-372">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="74212-373">Constantes MAPI adicionales</span><span class="sxs-lookup"><span data-stu-id="74212-373">Additional MAPI constants</span></span>

<span data-ttu-id="74212-374">Esta sección contiene las definiciones de constantes que incluyen códigos de error y los identificadores de interfaz usados por la API de MAPI que no se han expuesto y documentado previamente.</span><span class="sxs-lookup"><span data-stu-id="74212-374">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="74212-375">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="74212-375">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="74212-376">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="74212-376">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="74212-377">Cuando un cliente llama al método [IAddrBook::Details](iaddrbook-details.md), el cliente debe configurar la marca **DIALOG_MODAL** en el parámetro _ulFlags_ parámetro para mostrar el cuadro de diálogo modal con los detalles sobre una entrada de la libreta de direcciones determinada.</span><span class="sxs-lookup"><span data-stu-id="74212-377">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="74212-378">Esta constante se define en mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="74212-378">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="74212-379">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="74212-379">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="74212-380">0x00000800</span><span class="sxs-lookup"><span data-stu-id="74212-380">0x00000800</span></span>  <br/> |<span data-ttu-id="74212-381">En Outlook 2007, los almacenes de archivos PST ajustados procesan los nuevos mensajes con filtros de spam y reglas antes de que se notifique a los clientes de MAPI de los mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="74212-381">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="74212-382">.Un proveedor o un cliente que use el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)  para crear un nuevo mensaje en los almacenes PST debe establecer la marca **ITEMPROC_FORCE** en el parámetro _ulFlags_ del método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para indicar al almacén de archivos PST que el mensaje es apto para el procesamiento de reglas antes de que el almacén notifique a cualquier cliente en escucha de la llegada del nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="74212-382">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="74212-383">Tenga en cuenta que dichas reglas de procesamiento solo se aplican a los nuevos mensajes creados en un servidor que no sea un Microsoft Exchange Server, ya que Exchange Server procesa las reglas para los mensajes en el servidor.</span><span class="sxs-lookup"><span data-stu-id="74212-383">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="74212-384">Por lo tanto, el proveedor o cliente que crea un mensaje debe pasar este indicador junto con **NON_EMS_XP_SAVE**, lo que indica que el servidor no es un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="74212-384">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="74212-385">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="74212-385">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="74212-386">0x00200000</span><span class="sxs-lookup"><span data-stu-id="74212-386">0x00200000</span></span>  <br/> |<span data-ttu-id="74212-387">Un cliente puede llamar a la función [MAPILogonEx](mapilogonex.md), configurando la marca **MAPI_BG_SESSION** en el parámetro _flFlags_ para iniciar una sesión y llevar a cabo cualquier operación en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="74212-387">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="74212-388">En general, si un cliente pretende realizar procesamiento en un subproceso en segundo plano o en un proceso independiente de manera que no altere el subproceso de primer plano, debe llamar a [MAPILogonEx](mapilogonex.md) con la marca **MAPI_BG_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="74212-388">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="74212-389">Un ejemplo en el que se utiliza es una aplicación de cliente, como un motor de indexación, que abre un archivo de carpetas personales (PST) para un acceso de fondo.</span><span class="sxs-lookup"><span data-stu-id="74212-389">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="74212-390">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="74212-390">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="74212-391">0x00004000</span><span class="sxs-lookup"><span data-stu-id="74212-391">0x00004000</span></span>  <br/> |<span data-ttu-id="74212-392">Un cliente puede llamar al método [IAddrBook::OpenEntry](iaddrbook-openentry.md), estableciendo la marca **MAPI_CACHE_ONLY** en el parámetro _ulFlags_ para abrir una entrada de la libreta de direcciones y posteriormente obtener acceso a ella solo desde la caché.</span><span class="sxs-lookup"><span data-stu-id="74212-392">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="74212-393">Un ejemplo en el que se utiliza es una aplicación de cliente que quiere abrir la lista global de direcciones en el modo caché de Exchange y obtener acceso a una entrada de esa libreta de direcciones de la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="74212-393">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="74212-394">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="74212-394">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="74212-395">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="74212-395">0x0000000C</span></span>  <br/> |<span data-ttu-id="74212-396">Este valor puede pasarse a la función MAPISendMail de Simple MAPI en el parámetro _ulFlags_ para especificar que se muestra un cuadro de diálogo sin modo mediante la aplicación de correo predeterminada.</span><span class="sxs-lookup"><span data-stu-id="74212-396">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="74212-397">Si no se establecen ni este indicador ni MAPI_DIALOG (0 x 00000008), no se mostrará ningún cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="74212-397">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="74212-398">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="74212-398">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="74212-399">0x00000200</span><span class="sxs-lookup"><span data-stu-id="74212-399">0x00000200</span></span>  <br/> |<span data-ttu-id="74212-400">Si Microsoft Office Outlook está en modo caché de Exchange y se ha abierto un almacén en modo caché, un cliente o proveedor de servicios puede llamar a [IMsgStore::OpenEntry](imsgstore-openentry.md), estableciendo la marca **MAPI_NO_CACHE** en el parámetro _ulFlags_ para abrir un elemento o una carpeta en el almacén remoto.</span><span class="sxs-lookup"><span data-stu-id="74212-400">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="74212-401">Tenga en cuenta que, si abre el almacén de mensajes con la marca **MDB_ONLINE** en el servidor remoto, no tiene que usar la marca **MAPI_NO_CACHE**.</span><span class="sxs-lookup"><span data-stu-id="74212-401">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="74212-402">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="74212-402">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="74212-403">0x80000000</span><span class="sxs-lookup"><span data-stu-id="74212-403">0x80000000</span></span>  <br/> |<span data-ttu-id="74212-404">Un cliente o proveedor de servicios puede llamar a la función [OpenIMsgOnIStg](openimsgonistg.md), configurando la marca **MAPI_UNICODE** en el parámetro _ulFlags_ para crear archivos .msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="74212-404">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="74212-405">El archivo [IMessage: IMAPIProp](imessageimapiprop.md) resultante muestra **STORE_UNICODE_OK** en su [Propiedad canónica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) y es compatible con propiedades Unicode.</span><span class="sxs-lookup"><span data-stu-id="74212-405">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="74212-406">Esta constante se define en mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="74212-406">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="74212-407">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="74212-407">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="74212-408">0x00000100</span><span class="sxs-lookup"><span data-stu-id="74212-408">0x00000100</span></span>  <br/> |<span data-ttu-id="74212-409">Si Outlook está en  modo caché de Exchange, un cliente o proveedor de servicios puede llamar al método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), estableciendo la marca **MDB_ONLINE** en el parámetro _ulFlags_ para invalidar la conexión con el almacén de mensajes locales y abrir el almacén en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="74212-409">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="74212-410">Tenga en cuenta que no puede abrir un almacén de Exchange en el modo caché y en modo sin caché al mismo tiempo en la misma sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="74212-410">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="74212-411">Si ya ha abierto el almacén de mensajes en modo caché, debe cerrar el almacén antes de abrirlo con esta marca o abrir una nueva sesión MAPI donde puede abrir el almacén de Exchange en el servidor remoto mediante este marcador.</span><span class="sxs-lookup"><span data-stu-id="74212-411">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="74212-412">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="74212-412">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="74212-413">0x00001000</span><span class="sxs-lookup"><span data-stu-id="74212-413">0x00001000</span></span>  <br/> |<span data-ttu-id="74212-414">Un cliente puede llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md), estableciendo la marca **NON_EMS_XP_SAVE** en el parámetro _ulFlags_ para indicar que el mensaje no se ha entregado desde un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="74212-414">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="74212-415">Esta marca puede usarse junto con la marca **ITEMPROC_FORCE** en el parámetro _ulFlags_ para indicar a un almacén PST que el mensaje es apto para el procesamiento de reglas antes de que el almacén PST notifique  a cualquier cliente en escucha de la llegada del mensaje.</span><span class="sxs-lookup"><span data-stu-id="74212-415">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="74212-416">Esto reglas de procesamiento solo se aplican a los nuevos mensajes creados con [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en un servidor que no es un servidor de Exchange (en cuyo caso el servidor Exchange ya habría procesado reglas en el mensaje).</span><span class="sxs-lookup"><span data-stu-id="74212-416">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="74212-417">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="74212-417">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="74212-418">0x00000080</span><span class="sxs-lookup"><span data-stu-id="74212-418">0x00000080</span></span>  <br/> |<span data-ttu-id="74212-419">Un cliente puede llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md), estableciendo la marca **SPAMFILTER_ONSAVE** en el parámetro _ulFlags_ para habilitar el filtrado de spam en un mensaje que se está guardando.</span><span class="sxs-lookup"><span data-stu-id="74212-419">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="74212-420">El soporte de filtrado de spam solo está disponible si el tipo de dirección de correo electrónico del remitente es Protocolo simple de transferencia de correo (SMTP) y el mensaje se está guardando en un almacén de un archivo de carpetas personales (PST).</span><span class="sxs-lookup"><span data-stu-id="74212-420">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="74212-421">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="74212-421">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="74212-422">0x00200000</span><span class="sxs-lookup"><span data-stu-id="74212-422">0x00200000</span></span>  <br/> |<span data-ttu-id="74212-423">Si se establece esta marca en la [Propiedad canónica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) de un almacén de archivos PST ajustado, indica que cuando llega un mensaje nuevo al almacén, el almacén procesa reglas y filtrado antispam del mensaje por separado.</span><span class="sxs-lookup"><span data-stu-id="74212-423">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="74212-424">A continuación el almacén llama a [IMAPISupport::Notify](imapisupport-notify.md), configurando **fnevNewMail** en la estructura [notificación](notification.md) estructura que se pasa como un parámetro y pasando los detalles del nuevo mensaje a un cliente en escucha.</span><span class="sxs-lookup"><span data-stu-id="74212-424">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="74212-425">Posteriormente, cuando el cliente en escucha recibe la notificación, no procesa las reglas en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="74212-425">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="74212-426">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="74212-426">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="74212-427">0x00040000</span><span class="sxs-lookup"><span data-stu-id="74212-427">0x00040000</span></span>  <br/> |<span data-ttu-id="74212-428">Si esta marca se incluye en la [Propiedad canónica PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), indica que el almacén admite almacenamiento Unicode.</span><span class="sxs-lookup"><span data-stu-id="74212-428">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="74212-429">Un cliente puede buscar la presencia de la marca para decidir si desea solicitar o guardar información Unicode en el almacén.</span><span class="sxs-lookup"><span data-stu-id="74212-429">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="74212-430">Definiciones para archivar elementos en una carpeta</span><span class="sxs-lookup"><span data-stu-id="74212-430">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="74212-431">Las siguientes definiciones de constantes son valores que se usan para configurar la [Propiedad canónica PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="74212-431">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="74212-432">Definiciones para mostrar objetos remotos</span><span class="sxs-lookup"><span data-stu-id="74212-432">Definitions for displaying remote objects</span></span>

<span data-ttu-id="74212-433">Las definiciones de macros y constantes siguientes son para mostrar los objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="74212-433">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="74212-434">Para obtener más información, vea la [Propiedad canónica PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="74212-434">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="74212-435">Definiciones de libreta de direcciones de Exchange y códigos de error del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="74212-435">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="74212-436">A continuación se muestran las definiciones de códigos de error de la libreta de direcciones de Exchange y el almacén de mensajes, que tienen capacidad de reconexión.</span><span class="sxs-lookup"><span data-stu-id="74212-436">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="74212-437">La última llamada a un catálogo global (GC) desconectado puede dar como resultado el error **MAPI_E_END_OF_SESSION**, que debería volverse a intentar.</span><span class="sxs-lookup"><span data-stu-id="74212-437">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="74212-438">MAPI de Outlook es compatible con la reconexión a un servidor de catálogo global sin reconfiguración especial, pero puede que se devuelvan otros códigos de error al cliente.</span><span class="sxs-lookup"><span data-stu-id="74212-438">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="74212-439">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="74212-439">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="74212-440">0x80040200</span><span class="sxs-lookup"><span data-stu-id="74212-440">0x80040200</span></span>  <br/> |<span data-ttu-id="74212-441">Se devuelve cuando se ha desconectado una conexión.</span><span class="sxs-lookup"><span data-stu-id="74212-441">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="74212-442">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="74212-442">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="74212-443">0x80040125</span><span class="sxs-lookup"><span data-stu-id="74212-443">0x80040125</span></span>  <br/> |<span data-ttu-id="74212-444">Se devuelve cuando el token de conexión de llamada a procedimiento remoto (RPC) no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="74212-444">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="74212-445">Si el token de la transacción actual es diferente del token de la conexión, significa que se ha vuelto a conectar, por lo que se devuelve **MAPI_E_RECONNECTED** y se puede tratar del mismo modo que **MAPI_E_END_OF_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="74212-445">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="74212-446">Debería volver a intentar la llamada.</span><span class="sxs-lookup"><span data-stu-id="74212-446">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="74212-447">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="74212-447">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="74212-448">0x80040126</span><span class="sxs-lookup"><span data-stu-id="74212-448">0x80040126</span></span>  <br/> |<span data-ttu-id="74212-449">Se devuelve cuando la conexión está desconectada.</span><span class="sxs-lookup"><span data-stu-id="74212-449">Returned when the connection is offline.</span></span> <span data-ttu-id="74212-450">Normalmente, esto significa que ha ocurrido algo en el entorno, como errores en el servidor o pérdida de conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="74212-450">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="74212-451">Es más probable que aparezca este error al usar el modo caché de un perfil e intenta evitar la caché para comunicarse con el servidor.</span><span class="sxs-lookup"><span data-stu-id="74212-451">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="74212-452">Si la caché no pudo inicialmente establecer una conexión con el servidor, puede que esté en el estado sin conexión en el que **MAPI_E_OFFLINE** puede aparecer.</span><span class="sxs-lookup"><span data-stu-id="74212-452">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="74212-453">Ninguno de los dos errores anteriores se devolverán en todos los escenarios donde parece probable que se aplicasen.</span><span class="sxs-lookup"><span data-stu-id="74212-453">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="74212-454">En la mayoría de los casos, se devolverán **MAPI\_E_NETWORK_ERROR** o **MAPI_E_CALL_FAILED**.</span><span class="sxs-lookup"><span data-stu-id="74212-454">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="74212-455">Ninguno aparecerá al usar la descarga de [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440).</span><span class="sxs-lookup"><span data-stu-id="74212-455">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="74212-456">Definiciones para las cuotas del modo de almacenamiento en caché del buzón de correo Exchange Server</span><span class="sxs-lookup"><span data-stu-id="74212-456">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="74212-457">Las siguientes definiciones de constantes son usadas por Microsoft Outlook 2010 y Microsoft Outlook 2013 para configurar las cuotas del perfil en modo caché de Exchange que son equivalentes a las cuotas de buzón de Exchange que, en caso contrario, sólo están disponibles con un perfil en línea.</span><span class="sxs-lookup"><span data-stu-id="74212-457">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="74212-458">Estas propiedades se asignan a sus propiedades en línea correspondientes y contienen los mismos valores en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="74212-458">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="74212-459">PR_QUOTA_WARNING se asigna a PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND a PR_QUOTA_PROHIBIT_SEND_QUOTA y PR_QUOTA_RECEIVE a PR_PROHIBIT_RECEIVE_QUOTA.</span><span class="sxs-lookup"><span data-stu-id="74212-459">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="74212-460">Definiciones de formato del mensaje</span><span class="sxs-lookup"><span data-stu-id="74212-460">Definitions for message format</span></span>

<span data-ttu-id="74212-461">Las siguientes definiciones de constantes son valores que se usan para configurar la [Propiedad canónica PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="74212-461">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="74212-462">Definiciones para usar RPC a través de HTTP</span><span class="sxs-lookup"><span data-stu-id="74212-462">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="74212-463">Consulte el tema [Propiedad canónica PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) para obtener definiciones de constantes usadas como marcas para establecer la propiedad.</span><span class="sxs-lookup"><span data-stu-id="74212-463">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="74212-464">Consulte el tema [Propiedad canónica PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) para obtener definiciones de constantes usadas para establecer la propiedad.</span><span class="sxs-lookup"><span data-stu-id="74212-464">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="74212-465">Identificadores</span><span class="sxs-lookup"><span data-stu-id="74212-465">Identifiers</span></span>

<span data-ttu-id="74212-466">Use la macro `DEFINE_OLEGUID` definida en el archivo de encabezado guiddef.h del Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar los siguientes nombres simbólicos GUID a sus valores.</span><span class="sxs-lookup"><span data-stu-id="74212-466">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="74212-467">El siguiente identificador es para la sección de perfil Capone de una libreta de direcciones, que como apoyo a buzones múltiples de Exchange ([MultiEx](using-multiple-exchange-accounts.md)) contiene una propiedad [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) que desactiva de forma efectiva el contenedor predeterminado especificado por [SetDefaultDir](iaddrbook-setdefaultdir.md).</span><span class="sxs-lookup"><span data-stu-id="74212-467">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="74212-468">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="74212-468">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="74212-469">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="74212-469">IMAPISync</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="74212-470">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="74212-470">IMAPISyncProgressCallback</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a><span data-ttu-id="74212-471">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="74212-471">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a><span data-ttu-id="74212-472">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="74212-472">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a><span data-ttu-id="74212-473">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="74212-473">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="74212-474">Identificadores de interfaz del controlador de invalidación PST</span><span class="sxs-lookup"><span data-stu-id="74212-474">PST Override Handler interface identifiers</span></span>

#### <a name="iidipstoverridereq"></a><span data-ttu-id="74212-475">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="74212-475">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a><span data-ttu-id="74212-476">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="74212-476">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="74212-477">Vea también</span><span class="sxs-lookup"><span data-stu-id="74212-477">See also</span></span>

- [<span data-ttu-id="74212-478">Acerca de las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="74212-478">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="74212-479">Acerca de las propiedades con nombre que usa Outlook</span><span class="sxs-lookup"><span data-stu-id="74212-479">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="74212-480">Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="74212-480">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="74212-481">Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="74212-481">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="74212-482">Administrar un mensaje en un OST sin invocar una sincronización en el modo de intercambio en caché</span><span class="sxs-lookup"><span data-stu-id="74212-482">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

