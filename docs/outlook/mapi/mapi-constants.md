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
ms.openlocfilehash: d6d6c55776c1379ec1dab0e9a6f7ef0943d2480e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818104"
---
# <a name="mapi-constants"></a><span data-ttu-id="d1182-103">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d1182-103">MAPI constants</span></span>

<span data-ttu-id="d1182-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1182-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1182-105">Este tema contiene las definiciones de constantes, declaraciones de interfaz MAPI y los identificadores de clase e interfaz usados por la API de MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1182-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="d1182-106">Identificadores de clase e interfaz</span><span class="sxs-lookup"><span data-stu-id="d1182-106">Class and interface identifiers</span></span>

<span data-ttu-id="d1182-107">Use la macro DEFINE_GUID definida en el guiddef.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar los nombres simbólicos de identificador único global (GUID) con sus valores, a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="d1182-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="d1182-108">La API de conversión de seguridad de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="d1182-108">Attachment security conversion API</span></span>

<span data-ttu-id="d1182-109">Esta sección contiene las definiciones de constantes y los identificadores de interfaz para la API de seguridad de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d1182-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="d1182-110">Use la macro MAPIMETHOD definida en el mapidefs.h de archivo de encabezado de Windows SDK para definir la función virtual pura **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span><span class="sxs-lookup"><span data-stu-id="d1182-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="d1182-111">Use la macro DECLARE_MAPI_INTERFACE_ definida en el mapidefs.h de archivo de encabezado de Windows SDK para definir la tabla de método virtual para **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="d1182-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="d1182-112">La API de conversión de MIME a MAPI</span><span class="sxs-lookup"><span data-stu-id="d1182-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="d1182-113">Esta sección contiene las definiciones de constantes y los identificadores de clase e interfaz de la API de conversión de MIME a MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1182-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="d1182-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="d1182-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1182-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="d1182-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="d1182-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="d1182-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="d1182-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="d1182-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="d1182-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="d1182-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="d1182-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="d1182-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="d1182-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="d1182-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="d1182-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="d1182-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="d1182-122">0 x 0020</span><span class="sxs-lookup"><span data-stu-id="d1182-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="d1182-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="d1182-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="d1182-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="d1182-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="d1182-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="d1182-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="d1182-126">0 x 0080</span><span class="sxs-lookup"><span data-stu-id="d1182-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="d1182-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="d1182-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="d1182-128">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="d1182-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="d1182-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="d1182-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="d1182-130">0 x 4000</span><span class="sxs-lookup"><span data-stu-id="d1182-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="d1182-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d1182-131">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="d1182-132">*Tal como se define en el archivo winerror.h archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="d1182-132">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="d1182-133">Identificadores de clase</span><span class="sxs-lookup"><span data-stu-id="d1182-133">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="d1182-134">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="d1182-134">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="d1182-135">API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="d1182-135">Offline State API</span></span>

<span data-ttu-id="d1182-136">Esta sección contiene las definiciones de constantes y los identificadores de clase e interfaz de la API de estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d1182-136">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="d1182-137">Constantes</span><span class="sxs-lookup"><span data-stu-id="d1182-137">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1182-138">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d1182-138">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="d1182-139">*Tal como se define en el archivo winerror.h archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="d1182-139">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="d1182-140">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="d1182-140">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="d1182-141">*Tal como se define en el archivo winerror.h archivo de encabezado de Windows (SDK)*</span><span class="sxs-lookup"><span data-stu-id="d1182-141">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="d1182-142">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d1182-142">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="d1182-143">0 (ULONG)</span><span class="sxs-lookup"><span data-stu-id="d1182-143">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="d1182-144">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d1182-144">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="d1182-145">0 (ULONG)</span><span class="sxs-lookup"><span data-stu-id="d1182-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="d1182-146">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="d1182-146">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="d1182-147">1</span><span class="sxs-lookup"><span data-stu-id="d1182-147">1</span></span>  <br/> |
|<span data-ttu-id="d1182-148">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="d1182-148">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="d1182-149">0 x 1</span><span class="sxs-lookup"><span data-stu-id="d1182-149">0x1</span></span>  <br/> |
|<span data-ttu-id="d1182-150">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="d1182-150">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="d1182-151">0 x 2</span><span class="sxs-lookup"><span data-stu-id="d1182-151">0x2</span></span>  <br/> |
|<span data-ttu-id="d1182-152">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="d1182-152">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="d1182-153">0 x 00002000</span><span class="sxs-lookup"><span data-stu-id="d1182-153">0x00002000</span></span>  <br/> |
|<span data-ttu-id="d1182-154">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d1182-154">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="d1182-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1182-155">0x00000000</span></span>  <br/> |
|<span data-ttu-id="d1182-156">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="d1182-156">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="d1182-157">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="d1182-157">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="d1182-158">**En línea o sin conexión**</span><span class="sxs-lookup"><span data-stu-id="d1182-158">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="d1182-159">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="d1182-159">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="d1182-160">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="d1182-160">0x00000003</span></span>  <br/> |
|<span data-ttu-id="d1182-161">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="d1182-161">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="d1182-162">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1182-162">0x00000001</span></span>  <br/> |
|<span data-ttu-id="d1182-163">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="d1182-163">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="d1182-164">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d1182-164">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="d1182-165">Identificadores de clase</span><span class="sxs-lookup"><span data-stu-id="d1182-165">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="d1182-166">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="d1182-166">Interface identifiers</span></span>

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

## <a name="outlook-named-properties"></a><span data-ttu-id="d1182-167">Propiedades con nombre de Outlook</span><span class="sxs-lookup"><span data-stu-id="d1182-167">Outlook named properties</span></span>

<span data-ttu-id="d1182-168">Esta sección contiene las definiciones de constantes para las propiedades con nombre y su espacio de nombres y las otras constantes relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d1182-168">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="d1182-169">Definiciones de propiedades con nombre</span><span class="sxs-lookup"><span data-stu-id="d1182-169">Definitions for named properties</span></span>

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

### <a name="definitions-for-namespaces"></a><span data-ttu-id="d1182-170">Definiciones de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="d1182-170">Definitions for namespaces</span></span>

<span data-ttu-id="d1182-171">Los siguientes identificadores únicos (globales GUID) representan los espacios de nombres de las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="d1182-171">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
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

<span data-ttu-id="d1182-172">Hacer referencia a la sección almacén MAPI para las definiciones de PSETID.</span><span class="sxs-lookup"><span data-stu-id="d1182-172">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="d1182-173">Otras constantes</span><span class="sxs-lookup"><span data-stu-id="d1182-173">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1182-174">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="d1182-174">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="d1182-175">0xD000000</span><span class="sxs-lookup"><span data-stu-id="d1182-175">0xD000000</span></span>  <br/> |
|<span data-ttu-id="d1182-176">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="d1182-176">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="d1182-177">0x2000000</span><span class="sxs-lookup"><span data-stu-id="d1182-177">0x2000000</span></span>  <br/> |
|<span data-ttu-id="d1182-178">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="d1182-178">MNID_ID</span></span>  <br/> | <span data-ttu-id="d1182-179">*Tal como se define en el mapidefs.h del archivo de encabezado.*</span><span class="sxs-lookup"><span data-stu-id="d1182-179">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="d1182-180">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="d1182-180">MNID_STRING</span></span>  <br/> | <span data-ttu-id="d1182-181">*Tal como se define en el mapidefs.h del archivo de encabezado.*</span><span class="sxs-lookup"><span data-stu-id="d1182-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="d1182-182">mtgNone</span><span class="sxs-lookup"><span data-stu-id="d1182-182">mtgNone</span></span>  <br/> |<span data-ttu-id="d1182-183">0 x 0</span><span class="sxs-lookup"><span data-stu-id="d1182-183">0x0</span></span>  <br/> |
|<span data-ttu-id="d1182-184">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="d1182-184">mtgRequest</span></span>  <br/> |<span data-ttu-id="d1182-185">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1182-185">0x00000001</span></span>  <br/> |
|<span data-ttu-id="d1182-186">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="d1182-186">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="d1182-187">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-187">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-188">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="d1182-188">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="d1182-189">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="d1182-189">0x00020000</span></span>  <br/> |
|<span data-ttu-id="d1182-190">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="d1182-190">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="d1182-191">0 x 00080000</span><span class="sxs-lookup"><span data-stu-id="d1182-191">0x00080000</span></span>  <br/> |
|<span data-ttu-id="d1182-192">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="d1182-192">mtgDelegated</span></span>  <br/> |<span data-ttu-id="d1182-193">0 x 00100000</span><span class="sxs-lookup"><span data-stu-id="d1182-193">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="d1182-194">API de replicación</span><span class="sxs-lookup"><span data-stu-id="d1182-194">Replication API</span></span>

<span data-ttu-id="d1182-195">Esta sección contiene las definiciones de constantes, declaraciones de interfaz MAPI e identificadores de clase e interfaz para la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="d1182-195">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="d1182-196">Constantes</span><span class="sxs-lookup"><span data-stu-id="d1182-196">Constants</span></span>

<span data-ttu-id="d1182-197">La siguiente es una estructura [MAPIUID](mapiuid.md) que identifica un proveedor de servicios MAPI:</span><span class="sxs-lookup"><span data-stu-id="d1182-197">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="d1182-198">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-198">DNH_OK</span></span>  <br/> |<span data-ttu-id="d1182-199">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-199">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-200">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-200">DNT_OK</span></span>  <br/> |<span data-ttu-id="d1182-201">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-202">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d1182-202">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="d1182-203">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="d1182-203">0x00000008</span></span>  <br/> |
|<span data-ttu-id="d1182-204">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="d1182-204">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="d1182-205">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="d1182-205">0x00000010</span></span>  <br/> |
|<span data-ttu-id="d1182-206">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-206">HSF_OK</span></span>  <br/> |<span data-ttu-id="d1182-207">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-207">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-208">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d1182-208">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="d1182-209">((ULONG) 0X00000800)</span><span class="sxs-lookup"><span data-stu-id="d1182-209">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="d1182-210">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="d1182-210">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="d1182-211">((ULONG) 0 X 00001000)</span><span class="sxs-lookup"><span data-stu-id="d1182-211">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="d1182-212">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="d1182-212">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="d1182-213">((ULONG) 0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="d1182-213">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="d1182-214">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="d1182-214">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="d1182-215">0</span><span class="sxs-lookup"><span data-stu-id="d1182-215">0</span></span>  <br/> |
|<span data-ttu-id="d1182-216">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="d1182-216">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="d1182-217">1</span><span class="sxs-lookup"><span data-stu-id="d1182-217">1</span></span>  <br/> |
|<span data-ttu-id="d1182-218">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="d1182-218">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="d1182-219">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1182-219">0x00000001</span></span>  <br/> |
|<span data-ttu-id="d1182-220">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="d1182-220">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="d1182-221">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d1182-221">0x00000002</span></span>  <br/> |
|<span data-ttu-id="d1182-222">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="d1182-222">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="d1182-223">0x00000040</span><span class="sxs-lookup"><span data-stu-id="d1182-223">0x00000040</span></span>  <br/> |
|<span data-ttu-id="d1182-224">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="d1182-224">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="d1182-225">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d1182-225">0x00000080</span></span>  <br/> |
|<span data-ttu-id="d1182-226">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="d1182-226">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="d1182-227">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="d1182-227">0x00000200</span></span>  <br/> |
|<span data-ttu-id="d1182-228">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="d1182-228">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="d1182-229">0 x 00001000</span><span class="sxs-lookup"><span data-stu-id="d1182-229">0x00001000</span></span>  <br/> |
|<span data-ttu-id="d1182-230">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="d1182-230">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="d1182-231">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="d1182-231">0x00020000</span></span>  <br/> |
|<span data-ttu-id="d1182-232">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="d1182-232">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="d1182-233">0x02000000</span><span class="sxs-lookup"><span data-stu-id="d1182-233">0x02000000</span></span>  <br/> |
|<span data-ttu-id="d1182-234">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-234">UPC_OK</span></span>  <br/> |<span data-ttu-id="d1182-235">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-235">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-236">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="d1182-236">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="d1182-237">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1182-237">0x00000001</span></span>  <br/> |
|<span data-ttu-id="d1182-238">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="d1182-238">UPD_MOV</span></span>  <br/> |<span data-ttu-id="d1182-239">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d1182-239">0x00000002</span></span>  <br/> |
|<span data-ttu-id="d1182-240">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-240">UPD_OK</span></span>  <br/> |<span data-ttu-id="d1182-241">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-241">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-242">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="d1182-242">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="d1182-243">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="d1182-243">0x00020000</span></span>  <br/> |
|<span data-ttu-id="d1182-244">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="d1182-244">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="d1182-245">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="d1182-245">0x00040000</span></span>  <br/> |
|<span data-ttu-id="d1182-246">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="d1182-246">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="d1182-247">0 x 00080000</span><span class="sxs-lookup"><span data-stu-id="d1182-247">0x00080000</span></span>  <br/> |
|<span data-ttu-id="d1182-248">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="d1182-248">UPF_NEW</span></span>  <br/> |<span data-ttu-id="d1182-249">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1182-249">0x00000001</span></span>  <br/> |
|<span data-ttu-id="d1182-250">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="d1182-250">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="d1182-251">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d1182-251">0x00000002</span></span>  <br/> |
|<span data-ttu-id="d1182-252">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="d1182-252">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="d1182-253">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="d1182-253">0x00000004</span></span>  <br/> |
|<span data-ttu-id="d1182-254">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="d1182-254">UPF_DEL</span></span>  <br/> |<span data-ttu-id="d1182-255">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="d1182-255">0x00000008</span></span>  <br/> |
|<span data-ttu-id="d1182-256">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-256">UPF_OK</span></span>  <br/> |<span data-ttu-id="d1182-257">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-257">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-258">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-258">UPH_OK</span></span>  <br/> |<span data-ttu-id="d1182-259">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-260">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="d1182-260">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="d1182-261">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1182-261">0x00000001</span></span>  <br/> |
|<span data-ttu-id="d1182-262">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="d1182-262">UPM_NEW</span></span>  <br/> |<span data-ttu-id="d1182-263">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d1182-263">0x00000002</span></span>  <br/> |
|<span data-ttu-id="d1182-264">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="d1182-264">UPM_MOV</span></span>  <br/> |<span data-ttu-id="d1182-265">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="d1182-265">0x00000004</span></span>  <br/> |
|<span data-ttu-id="d1182-266">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="d1182-266">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="d1182-267">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="d1182-267">0x00000008</span></span>  <br/> |
|<span data-ttu-id="d1182-268">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="d1182-268">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="d1182-269">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="d1182-269">0x00000010</span></span>  <br/> |
|<span data-ttu-id="d1182-270">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-270">UPM_OK</span></span>  <br/> |<span data-ttu-id="d1182-271">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-271">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-272">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="d1182-272">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="d1182-273">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="d1182-273">0x00020000</span></span>  <br/> |
|<span data-ttu-id="d1182-274">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="d1182-274">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="d1182-275">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="d1182-275">0x00040000</span></span>  <br/> |
|<span data-ttu-id="d1182-276">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="d1182-276">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="d1182-277">0 x 00080000</span><span class="sxs-lookup"><span data-stu-id="d1182-277">0x00080000</span></span>  <br/> |
|<span data-ttu-id="d1182-278">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="d1182-278">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="d1182-279">0 x 00100000</span><span class="sxs-lookup"><span data-stu-id="d1182-279">0x00100000</span></span>  <br/> |
|<span data-ttu-id="d1182-280">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="d1182-280">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="d1182-281">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1182-281">0x00000001</span></span>  <br/> |
|<span data-ttu-id="d1182-282">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="d1182-282">UPR_READ</span></span>  <br/> |<span data-ttu-id="d1182-283">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d1182-283">0x00000002</span></span>  <br/> |
|<span data-ttu-id="d1182-284">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-284">UPR_OK</span></span>  <br/> |<span data-ttu-id="d1182-285">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-285">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-286">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="d1182-286">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="d1182-287">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="d1182-287">0x00020000</span></span>  <br/> |
|<span data-ttu-id="d1182-288">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="d1182-288">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="d1182-289">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1182-289">0x00000001</span></span>  <br/> |
|<span data-ttu-id="d1182-290">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="d1182-290">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="d1182-291">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d1182-291">0x00000002</span></span>  <br/> |
|<span data-ttu-id="d1182-292">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="d1182-292">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="d1182-293">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="d1182-293">0x00000004</span></span>  <br/> |
|<span data-ttu-id="d1182-294">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="d1182-294">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="d1182-295">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d1182-295">0x00000080</span></span>  <br/> |
|<span data-ttu-id="d1182-296">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-296">UPS_OK</span></span>  <br/> |<span data-ttu-id="d1182-297">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-297">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-298">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-298">UPT_OK</span></span>  <br/> |<span data-ttu-id="d1182-299">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-300">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="d1182-300">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="d1182-301">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1182-301">0x00000001</span></span>  <br/> |
|<span data-ttu-id="d1182-302">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="d1182-302">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="d1182-303">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="d1182-303">0x00010000</span></span>  <br/> |
|<span data-ttu-id="d1182-304">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="d1182-304">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="d1182-305">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="d1182-305">0x00020000</span></span>  <br/> |
|<span data-ttu-id="d1182-306">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="d1182-306">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="d1182-307">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="d1182-307">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="d1182-308">Declaraciones de interfaz</span><span class="sxs-lookup"><span data-stu-id="d1182-308">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="d1182-309">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="d1182-309">Interface identifiers</span></span>

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

<span data-ttu-id="d1182-310">Usar los siguientes dos identificadores de interfaz con [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md)o [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir y pasar por alto cualquier verificación proveedor en un objeto de carpeta y un objeto de mensaje, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d1182-310">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="d1182-311">Almacén de MAPI</span><span class="sxs-lookup"><span data-stu-id="d1182-311">MAPI store</span></span>

<span data-ttu-id="d1182-312">Esta sección contiene las definiciones de constantes y los identificadores de interfaz usan las API de dicha interfaz con un almacén de MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1182-312">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="d1182-313">Constantes</span><span class="sxs-lookup"><span data-stu-id="d1182-313">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="d1182-314">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="d1182-314">fnevIndexing</span></span>  <br/> |<span data-ttu-id="d1182-315">((ULONG) 0 X 00010000)</span><span class="sxs-lookup"><span data-stu-id="d1182-315">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="d1182-316">Un proveedor de almacén puede especificar **fnevIndexing** en el miembro **ulEventType** de la estructura de **[notificación](notification.md)** para notificar el indizador que un objeto está preparado para la indización.</span><span class="sxs-lookup"><span data-stu-id="d1182-316">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="d1182-317">El miembro de la **información** de la estructura de **notificación** contiene una estructura **[EXTENDED_NOTIFICATION](extended_notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="d1182-317">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="d1182-318">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="d1182-318">FS_NONE</span></span>  <br/> |<span data-ttu-id="d1182-319">0 x 00</span><span class="sxs-lookup"><span data-stu-id="d1182-319">0x00</span></span>  <br/> |<span data-ttu-id="d1182-320">Un cliente puede llamar a **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** y verificación de la máscara de bits devuelto.</span><span class="sxs-lookup"><span data-stu-id="d1182-320">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="d1182-321">**FS_NONE** indica que la carpeta no es compatible con el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="d1182-321">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="d1182-322">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="d1182-322">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="d1182-323">0x01</span><span class="sxs-lookup"><span data-stu-id="d1182-323">0x01</span></span>  <br/> |<span data-ttu-id="d1182-324">Un cliente puede llamar a **IFolderSupport::GetSupportMask** y verificación de la máscara de bits devuelto.</span><span class="sxs-lookup"><span data-stu-id="d1182-324">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="d1182-325">**FS_SUPPORTS_SHARING** indica que la carpeta es compatible con el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="d1182-325">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="d1182-326">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="d1182-326">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="d1182-327">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="d1182-327">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="d1182-328">Identifica el proceso que es inserción de una notificación en un indizador que un objeto está preparado para la indización.</span><span class="sxs-lookup"><span data-stu-id="d1182-328">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="d1182-329">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="d1182-329">MNID_ID</span></span>  <br/> |<span data-ttu-id="d1182-330">Tal como se define en el mapidefs.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="d1182-330">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="d1182-331">Un valor para el campo **ulKind** de la estructura **[MAPINAMEID](mapinameid.md)** .</span><span class="sxs-lookup"><span data-stu-id="d1182-331">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="d1182-332">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="d1182-332">MNID_STRING</span></span>  <br/> |<span data-ttu-id="d1182-333">Tal como se define en el mapidefs.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d1182-333">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="d1182-334">Un valor para el campo **ulKind** de la estructura **[MAPINAMEID](mapinameid.md)** .</span><span class="sxs-lookup"><span data-stu-id="d1182-334">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="d1182-335">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="d1182-335">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="d1182-336">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="d1182-336">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="d1182-337">Si un cliente especifica **MSCAP_SEL_RESTRICTION** en *mscapSelector* para **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** puede devolver este valor si el almacén de pasa por alto los parámetros no válidos en una restricción.</span><span class="sxs-lookup"><span data-stu-id="d1182-337">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="d1182-338">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="d1182-338">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="d1182-339">((ULONG) 0 X 00000020)</span><span class="sxs-lookup"><span data-stu-id="d1182-339">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="d1182-340">Si un cliente especifica **MSCAP_SEL_FOLDER** en *mscapSelector* para **IMSCapabilities::GetCapabilities**, **GetCapabilities** puede devolver este valor si el almacén es un almacén no predeterminada que es compatible con las páginas principales de carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1182-340">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="d1182-341">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-341">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="d1182-342">((ULONG) 0X00800000)</span><span class="sxs-lookup"><span data-stu-id="d1182-342">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="d1182-343">Un cliente puede obtener la propiedad **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** para determinar las características de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d1182-343">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="d1182-344">Si el proveedor de almacenamiento establece la marca **STORE_PUSHER_OK** en la máscara de bits, que significa que el controlador de protocolo MAPI no va a rastrear el almacén y el almacén es responsable de los cambios a través de notificaciones de inserción al indizador para que los mensajes se indizan.</span><span class="sxs-lookup"><span data-stu-id="d1182-344">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="d1182-345">Definiciones de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="d1182-345">Definitions for namespaces</span></span>

<span data-ttu-id="d1182-346">Los siguientes identificadores únicos (globales GUID) representan los espacios de nombres de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="d1182-346">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="d1182-347">Que se indizan por el controlador de protocolo MAPI (PH) y se documentan como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d1182-347">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="d1182-348">Las propiedades con nombre no deben usarse para crear o modificar elementos.</span><span class="sxs-lookup"><span data-stu-id="d1182-348">The named properties should not be used to create or modify items.</span></span> 
  
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

#### <a name="mnidid-properties"></a><span data-ttu-id="d1182-349">Propiedades MNID_ID</span><span class="sxs-lookup"><span data-stu-id="d1182-349">MNID_ID Properties</span></span>
  
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

#### <a name="mnidstring-properties"></a><span data-ttu-id="d1182-350">Propiedades MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="d1182-350">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="d1182-351">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="d1182-351">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="d1182-352">Usar el `DEFINE_OLEGUID` macro definida en el guiddef.h de archivo de encabezado de Windows SDK para asociar el nombre simbólico de GUID siguiente con su valor.</span><span class="sxs-lookup"><span data-stu-id="d1182-352">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="d1182-353">Constantes de la libreta de direcciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="d1182-353">MAPI Address Book constants</span></span>

<span data-ttu-id="d1182-354">Esta sección contiene las definiciones de constantes para la libreta de direcciones de MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1182-354">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="d1182-355">Constantes</span><span class="sxs-lookup"><span data-stu-id="d1182-355">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="d1182-356">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="d1182-356">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="d1182-357">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="d1182-357">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="d1182-358">La carpeta raíz de un objeto de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1182-358">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="d1182-359">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="d1182-359">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="d1182-360">((ULONG) 0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="d1182-360">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="d1182-361">Una subcarpeta dentro de la carpeta raíz del objeto de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1182-361">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="d1182-362">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="d1182-362">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="d1182-363">((ULONG) 0 X 00000003)</span><span class="sxs-lookup"><span data-stu-id="d1182-363">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="d1182-364">Un objeto de contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d1182-364">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="d1182-365">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="d1182-365">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="d1182-366">((ULONG) 0 X 00000004)</span><span class="sxs-lookup"><span data-stu-id="d1182-366">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="d1182-367">Un objeto de usuario de mensajer�a.</span><span class="sxs-lookup"><span data-stu-id="d1182-367">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="d1182-368">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="d1182-368">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="d1182-369">((ULONG) 0 X 00000005)</span><span class="sxs-lookup"><span data-stu-id="d1182-369">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="d1182-370">Un objeto de lista de distribuci�n.</span><span class="sxs-lookup"><span data-stu-id="d1182-370">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="d1182-371">Constantes MAPI adicionales</span><span class="sxs-lookup"><span data-stu-id="d1182-371">Additional MAPI constants</span></span>

<span data-ttu-id="d1182-372">Esta sección contiene las definiciones de constantes incluidos los códigos de error y los identificadores de interfaz usados por las API de MAPI que anteriormente no se han expuesto y se documentan.</span><span class="sxs-lookup"><span data-stu-id="d1182-372">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="d1182-373">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="d1182-373">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="d1182-374">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="d1182-374">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="d1182-375">Cuando un cliente llama al método de [IAddrBook::Details](iaddrbook-details.md) , el cliente debe establecer la marca **DIALOG_MODAL** en el parámetro _ulFlags_ para mostrar el cuadro de diálogo modal que muestra los detalles acerca de una entrada de la libreta de direcciones determinada.</span><span class="sxs-lookup"><span data-stu-id="d1182-375">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="d1182-376">Esta constante se define en mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="d1182-376">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="d1182-377">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="d1182-377">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="d1182-378">0x00000800</span><span class="sxs-lookup"><span data-stu-id="d1182-378">0x00000800</span></span>  <br/> |<span data-ttu-id="d1182-379">En Outlook 2007, almacenes de archivos PST ajustados tengan reglas y filtrado de spam procesa en nuevos mensajes antes de que los clientes MAPI reciben notificaciones de los mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="d1182-379">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="d1182-380">Un proveedor o cliente mediante el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para crear un nuevo mensaje en almacenes de PST debe establecer la marca **ITEMPROC_FORCE** en el parámetro _ulFlags_ del método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para indicar a PST almacén de que el mensaje es apto para las reglas de procesamiento antes de que el almacén notifica a cualquier cliente de escucha de la llegada del nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="d1182-380">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="d1182-381">Tenga en cuenta que esas reglas de procesamiento sólo se aplica a los nuevos mensajes creados en un servidor que no es un servidor de Exchange de Microsoft, debido a que Exchange Server procesa las reglas para los mensajes en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d1182-381">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="d1182-382">Por lo tanto, el proveedor o cliente que crea el mensaje debe pasar esta marca en combinación con **NON_EMS_XP_SAVE**, que indica que el servidor no es un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d1182-382">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="d1182-383">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="d1182-383">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="d1182-384">0x00200000</span><span class="sxs-lookup"><span data-stu-id="d1182-384">0x00200000</span></span>  <br/> |<span data-ttu-id="d1182-385">Un cliente puede llamar a la función [MAPILogonEx](mapilogonex.md) , al establecer el indicador **MAPI_BG_SESSION** en el parámetro _flFlags_ para iniciar una sesión y realizar cualquier operación en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d1182-385">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="d1182-386">En general, si un cliente se va a realizar el procesamiento en un subproceso de fondo o en un proceso independiente de manera que sea discreto al subproceso de primer plano, debe llamar a [MAPILogonEx](mapilogonex.md) con la marca **MAPI_BG_SESSION** .</span><span class="sxs-lookup"><span data-stu-id="d1182-386">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="d1182-387">Un ejemplo donde se utiliza es una aplicación de cliente, como un motor de indización, abrir un archivo de carpetas personales (PST) para el acceso de tipo de fondo.</span><span class="sxs-lookup"><span data-stu-id="d1182-387">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="d1182-388">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="d1182-388">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="d1182-389">0x00004000</span><span class="sxs-lookup"><span data-stu-id="d1182-389">0x00004000</span></span>  <br/> |<span data-ttu-id="d1182-390">Un cliente puede llamar al método [IAddrBook::OpenEntry](iaddrbook-openentry.md) , al establecer el indicador **MAPI_CACHE_ONLY** en el parámetro _ulFlags indicado_ para abrir una entrada de la libreta de direcciones y tener acceso a él posteriormente sólo desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="d1182-390">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="d1182-391">Un ejemplo donde se utiliza es una aplicación cliente que desea abrir la lista Global de direcciones en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="d1182-391">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="d1182-392">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="d1182-392">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="d1182-393">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="d1182-393">0x0000000C</span></span>  <br/> |<span data-ttu-id="d1182-394">Este valor se puede pasar a la función MAPISendMail de Simple MAPI en el parámetro _ulFlags_ para especificar que se muestra un cuadro de diálogo no modal mediante la aplicación de correo predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d1182-394">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="d1182-395">Si se establece este indicador ni MAPI_DIALOG (0 x 00000008), no se muestra ningún cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d1182-395">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="d1182-396">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="d1182-396">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="d1182-397">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="d1182-397">0x00000200</span></span>  <br/> |<span data-ttu-id="d1182-398">Si Microsoft Office Outlook está en modo caché de Exchange y un almacén se ha abierto en modo en caché, puede llamar a un proveedor de servicio o cliente de [IMsgStore::OpenEntry](imsgstore-openentry.md), al establecer el indicador **MAPI_NO_CACHE** en el parámetro _ulFlags_ para abrir un elemento o una carpeta en el almacén remoto.</span><span class="sxs-lookup"><span data-stu-id="d1182-398">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="d1182-399">Tenga en cuenta que si se abre el almacén de mensajes con el indicador **MDB_ONLINE** en el servidor remoto, no es necesario usar el indicador **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="d1182-399">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="d1182-400">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d1182-400">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="d1182-401">0 x 80000000</span><span class="sxs-lookup"><span data-stu-id="d1182-401">0x80000000</span></span>  <br/> |<span data-ttu-id="d1182-402">Un proveedor de servicio o cliente puede llamar a la función [OpenIMsgOnIStg](openimsgonistg.md) , establecer el indicador **MAPI_UNICODE** en el parámetro _ulFlags_ para crear archivos .msg de Unicode.</span><span class="sxs-lookup"><span data-stu-id="d1182-402">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="d1182-403">El resultante [IMessage: IMAPIProp](imessageimapiprop.md) archivo muestra **STORE_UNICODE_OK** en su [Propiedad canónico PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) y es compatible con propiedades de Unicode.</span><span class="sxs-lookup"><span data-stu-id="d1182-403">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="d1182-404">Esta constante se define en mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="d1182-404">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="d1182-405">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="d1182-405">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="d1182-406">0 x 00000100</span><span class="sxs-lookup"><span data-stu-id="d1182-406">0x00000100</span></span>  <br/> |<span data-ttu-id="d1182-407">Si Outlook está en modo caché de Exchange, un proveedor de servicio o cliente puede llamar al método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) , al establecer el indicador **MDB_ONLINE** en el parámetro _ulFlags_ para invalidar la conexión con el almacén de mensajes local y abrir el almacén en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="d1182-407">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="d1182-408">Tenga en cuenta que no se puede abrir un almacén de Exchange en modo de caché y en modo sin caché al mismo tiempo en la misma sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="d1182-408">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="d1182-409">Si ya ha abierto el almacén de mensajes almacenados en caché, ya sea debe cerrar el almacén antes de que se abra con esta marca, o se abre una nueva sesión MAPI donde puede abrir el almacén de Exchange en el servidor remoto mediante el uso de esta marca.</span><span class="sxs-lookup"><span data-stu-id="d1182-409">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="d1182-410">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="d1182-410">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="d1182-411">0 x 00001000</span><span class="sxs-lookup"><span data-stu-id="d1182-411">0x00001000</span></span>  <br/> |<span data-ttu-id="d1182-412">Un cliente puede llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , al establecer el indicador **NON_EMS_XP_SAVE** en el parámetro _ulFlags_ para indicar que no se ha entregado el mensaje desde un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d1182-412">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="d1182-413">Este indicador se debe usar en combinación con el indicador **ITEMPROC_FORCE** en el parámetro _ulFlags_ para indicar a un almacén de archivos PST que el mensaje es apto para las reglas de procesamiento antes de la PST almacén notifica a cualquier cliente de escucha de la llegada de la Mensaje.</span><span class="sxs-lookup"><span data-stu-id="d1182-413">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="d1182-414">Esta regla de procesamiento sólo se aplica a los nuevos mensajes que se crean con [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en un servidor que no es un servidor de Exchange (en cuyo caso el servidor de Exchange ya habría procesa las reglas en el mensaje).</span><span class="sxs-lookup"><span data-stu-id="d1182-414">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="d1182-415">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="d1182-415">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="d1182-416">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d1182-416">0x00000080</span></span>  <br/> |<span data-ttu-id="d1182-417">Un cliente puede llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md), al establecer el indicador **SPAMFILTER_ONSAVE** en el parámetro _ulFlags_ para habilitar spam filtrado en un mensaje que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="d1182-417">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="d1182-418">Soporte técnico de filtrado de correo no está disponible sólo si el tipo de dirección de correo electrónico del remitente es el protocolo Simple de transferencia de correo (SMTP) y el mensaje se guarda en un almacén para un archivo de carpetas personales (PST).</span><span class="sxs-lookup"><span data-stu-id="d1182-418">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="d1182-419">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="d1182-419">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="d1182-420">0x00200000</span><span class="sxs-lookup"><span data-stu-id="d1182-420">0x00200000</span></span>  <br/> |<span data-ttu-id="d1182-421">Si este indicador se establece en la [Propiedad canónico PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) de un almacén de archivos PST ajustado, indica que cuando llegue un nuevo mensaje en el almacén, el almacén tiene reglas y filtrado de spam procesa por separado en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d1182-421">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="d1182-422">El almacén, a continuación, llama a [IMAPISupport::Notify](imapisupport-notify.md), establezca **fnevNewMail** en la estructura de [notificación](notification.md) que se pasa como un parámetro y pase los detalles del mensaje nuevo a un cliente de escucha.</span><span class="sxs-lookup"><span data-stu-id="d1182-422">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="d1182-423">Posteriormente, cuando el cliente escucha recibe la notificación, no se procesará las reglas en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d1182-423">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="d1182-424">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="d1182-424">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="d1182-425">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="d1182-425">0x00040000</span></span>  <br/> |<span data-ttu-id="d1182-426">Si este indicador se incluye en la [Propiedad canónico PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), indica que el almacén admite el almacenamiento de Unicode.</span><span class="sxs-lookup"><span data-stu-id="d1182-426">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="d1182-427">Un cliente puede buscar la presencia de la marca de decidir si va a solicitar o guardar información de Unicode en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="d1182-427">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="d1182-428">Definiciones de elementos en una carpeta de archivado</span><span class="sxs-lookup"><span data-stu-id="d1182-428">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="d1182-429">Las siguientes definiciones de constantes son valores que se usan para establecer la [Propiedad canónico PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="d1182-429">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="d1182-430">Definiciones para mostrar objetos remotos</span><span class="sxs-lookup"><span data-stu-id="d1182-430">Definitions for displaying remote objects</span></span>

<span data-ttu-id="d1182-431">Las siguientes definiciones de constante y la macro se utilizan para mostrar objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="d1182-431">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="d1182-432">Para obtener más información, vea la [Propiedad canónico PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="d1182-432">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="d1182-433">Las definiciones de la libreta de direcciones de Exchange y mensaje almacenan los códigos de error</span><span class="sxs-lookup"><span data-stu-id="d1182-433">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="d1182-434">El siguiente contiene las definiciones de código de error para la libreta de direcciones de Exchange y el almacén de mensajes, que tienen la capacidad de reconexión.</span><span class="sxs-lookup"><span data-stu-id="d1182-434">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="d1182-435">La última llamada a un catálogo Global (GC) desconectados puede provocar el error **MAPI_E_END_OF_SESSION** , que sería necesario volver a intentar.</span><span class="sxs-lookup"><span data-stu-id="d1182-435">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="d1182-436">MAPI admite reconexión de Outlook con un servidor de catálogo global sin reconfiguración especial, pero algún otro error códigos se pueden devolver al cliente.</span><span class="sxs-lookup"><span data-stu-id="d1182-436">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="d1182-437">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="d1182-437">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="d1182-438">0x80040200</span><span class="sxs-lookup"><span data-stu-id="d1182-438">0x80040200</span></span>  <br/> |<span data-ttu-id="d1182-439">Se devuelve cuando se ha desconectado una conexión.</span><span class="sxs-lookup"><span data-stu-id="d1182-439">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="d1182-440">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="d1182-440">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="d1182-441">0 x 80040125</span><span class="sxs-lookup"><span data-stu-id="d1182-441">0x80040125</span></span>  <br/> |<span data-ttu-id="d1182-442">Se devuelve cuando el símbolo (token) de conexión de llamada a procedimiento remoto (RPC) no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="d1182-442">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="d1182-443">Si el símbolo (token) de la transacción actual es diferente del símbolo (token) de la conexión que significa que se ha vuelto a conectar, por lo que **MAPI_E_RECONNECTED** se devuelve y se puede tratar de la misma como **MAPI_E_END_OF_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="d1182-443">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="d1182-444">Debe volver a intentar la llamada.</span><span class="sxs-lookup"><span data-stu-id="d1182-444">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="d1182-445">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="d1182-445">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="d1182-446">0x80040126</span><span class="sxs-lookup"><span data-stu-id="d1182-446">0x80040126</span></span>  <br/> |<span data-ttu-id="d1182-447">Se devuelve cuando la conexión está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d1182-447">Returned when the connection is offline.</span></span> <span data-ttu-id="d1182-448">Normalmente, esto significa que ha ocurrido algo en el entorno, como errores del servidor o la pérdida de conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="d1182-448">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="d1182-449">Este error es más probable que se producen cuando se usa el modo caché de un perfil y si se intenta omitir la memoria caché para comunicarse con el servidor.</span><span class="sxs-lookup"><span data-stu-id="d1182-449">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="d1182-450">Si la memoria caché nunca pudo establecer inicialmente una conexión con el servidor, puede ser en el estado sin conexión en el que podría exponer **MAPI_E_OFFLINE** .</span><span class="sxs-lookup"><span data-stu-id="d1182-450">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="d1182-451">Ninguno de los dos errores anteriores se devolverán en todos los escenarios donde es probable que aparecerían que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="d1182-451">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="d1182-452">En la mayoría de los casos, **MAPI\_E_NETWORK_ERROR** o se devolverá **MAPI_E_CALL_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="d1182-452">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="d1182-453">Ninguno de ellos aparecerá mediante la descarga de [Microsoft Exchange Server MAPI Client y Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) .</span><span class="sxs-lookup"><span data-stu-id="d1182-453">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="d1182-454">Cuotas de modo de caché de las definiciones para el buzón de correo de Exchange Server</span><span class="sxs-lookup"><span data-stu-id="d1182-454">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="d1182-455">Las siguientes definiciones de constantes usadas por Microsoft Outlook 2010 y Microsoft Outlook 2013 para establecer el intercambio en caché las cuotas de perfil de modo que son equivalentes a las cuotas de buzón de correo de Exchange en caso contrario, sólo está disponibles con un perfil en línea.</span><span class="sxs-lookup"><span data-stu-id="d1182-455">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="d1182-456">Estas propiedades se asignan a sus propiedades en línea consultará y contienen los mismos valores en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="d1182-456">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="d1182-457">PR_QUOTA_WARNING se asigna a PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND a PR_QUOTA_PROHIBIT_SEND_QUOTA y PR_QUOTA_RECEIVE a PR_PROHIBIT_RECEIVE_QUOTA.</span><span class="sxs-lookup"><span data-stu-id="d1182-457">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="d1182-458">Definiciones de formato de mensaje</span><span class="sxs-lookup"><span data-stu-id="d1182-458">Definitions for message format</span></span>

<span data-ttu-id="d1182-459">Las definiciones de constantes siguientes son valores que se usan para establecer la [Propiedad canónico PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="d1182-459">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="d1182-460">Definiciones para el uso de RPC sobre HTTP</span><span class="sxs-lookup"><span data-stu-id="d1182-460">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="d1182-461">Vea el tema de la [Propiedad canónico PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) para las definiciones de constantes utiliza como indicadores para establecer la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d1182-461">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="d1182-462">Vea el tema de la [Propiedad canónico PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) para las definiciones de constantes que se usa para establecer la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d1182-462">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="d1182-463">Identificadores</span><span class="sxs-lookup"><span data-stu-id="d1182-463">Identifiers</span></span>

<span data-ttu-id="d1182-464">Usar el `DEFINE_OLEGUID` macro definida en el guiddef.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar los nombres simbólicos de GUID siguientes con sus valores.</span><span class="sxs-lookup"><span data-stu-id="d1182-464">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="d1182-465">Es el identificador siguiente para la sección de perfil de Capone de una libreta de direcciones, que contiene una propiedad [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) que desactiva efectivamente el valor predeterminado de apoyo a varios buzones de Exchange ([MultiEx](using-multiple-exchange-accounts.md)) contenedor especificado por [SetDefaultDir](iaddrbook-setdefaultdir.md).</span><span class="sxs-lookup"><span data-stu-id="d1182-465">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="d1182-466">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="d1182-466">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="d1182-467">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="d1182-467">IMAPISync</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="d1182-468">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="d1182-468">IMAPISyncProgressCallback</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a><span data-ttu-id="d1182-469">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="d1182-469">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a><span data-ttu-id="d1182-470">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="d1182-470">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a><span data-ttu-id="d1182-471">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="d1182-471">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="d1182-472">Identificadores de interfaz de controlador de invalidar PST</span><span class="sxs-lookup"><span data-stu-id="d1182-472">PST Override Handler interface identifiers</span></span>

#### <a name="iidipstoverridereq"></a><span data-ttu-id="d1182-473">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="d1182-473">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a><span data-ttu-id="d1182-474">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="d1182-474">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="d1182-475">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1182-475">See also</span></span>

- [<span data-ttu-id="d1182-476">Información sobre las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="d1182-476">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="d1182-477">Información sobre las propiedades con nombre que usa Outlook</span><span class="sxs-lookup"><span data-stu-id="d1182-477">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="d1182-478">Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="d1182-478">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="d1182-479">Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="d1182-479">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="d1182-480">Administrar un mensaje en un OST sin invocar una sincronización en el modo de intercambio en caché</span><span class="sxs-lookup"><span data-stu-id="d1182-480">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

