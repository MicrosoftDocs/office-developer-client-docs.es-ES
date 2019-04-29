---
title: Constantes (API de disponibilidad)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Este tema contiene definiciones de constantes, identificadores de clase e identificadores de interfaz para la API de disponibilidad.
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431536"
---
# <a name="constants-freebusy-api"></a><span data-ttu-id="20731-103">Constantes (API de disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="20731-103">Constants (Free/busy API)</span></span>

<span data-ttu-id="20731-104">Este tema contiene definiciones de constantes, identificadores de clase e identificadores de interfaz para la API de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="20731-104">This topic contains constant definitions, class identifiers, and interface identifiers for the Free/Busy API.</span></span>
  
## <a name="constants"></a><span data-ttu-id="20731-105">Constantes</span><span class="sxs-lookup"><span data-stu-id="20731-105">Constants</span></span>

|<span data-ttu-id="20731-106">**Constante**</span><span class="sxs-lookup"><span data-stu-id="20731-106">**Constant**</span></span>|<span data-ttu-id="20731-107">**Definición**</span><span class="sxs-lookup"><span data-stu-id="20731-107">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20731-108">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="20731-108">E_NOTIMPL</span></span>  <br/> | <span data-ttu-id="20731-109">*Tal y como se define en el archivo de encabezado Winerror. h del kit de desarrollo de software (SDK) de Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="20731-109">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="20731-110">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="20731-110">E_OUTOFMEMORY</span></span>  <br/> | <span data-ttu-id="20731-111">*Como se define en el archivo de encabezado Winerror. h de Windows SDK.*</span><span class="sxs-lookup"><span data-stu-id="20731-111">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="20731-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="20731-112">S_FALSE</span></span>  <br/> | <span data-ttu-id="20731-113">*Como se define en el archivo de encabezado Winerror. h de Windows SDK.*</span><span class="sxs-lookup"><span data-stu-id="20731-113">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="20731-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="20731-114">S_OK</span></span>  <br/> | <span data-ttu-id="20731-115">*Como se define en el archivo de encabezado Winerror. h de Windows SDK.*</span><span class="sxs-lookup"><span data-stu-id="20731-115">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
   
## <a name="interface-identifiers"></a><span data-ttu-id="20731-116">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="20731-116">Interface identifiers</span></span>

<span data-ttu-id="20731-117">Para los siguientes identificadores de interfaz, asuma la macro DEFINE_GUID definida en el archivo de encabezado guiddef. h del SDK de Windows para asociar el nombre simbólico GUID con su valor.</span><span class="sxs-lookup"><span data-stu-id="20731-117">For the following interface identifiers, assume the DEFINE_GUID macro defined in the Windows SDK header file guiddef.h to associate the GUID symbolic name with its value.</span></span>
  
<span data-ttu-id="20731-118">{00067064-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="20731-118">//{00067064-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="20731-119">DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0X0, 0X0, 0xc0, 0X0, 0X0, 0X0, 0X0, 0X0, 0X0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="20731-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="20731-120">{00067066-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="20731-120">//{00067066-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="20731-121">DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0X0, 0X0, 0xc0, 0X0, 0X0, 0X0, 0X0, 0X0, 0X0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="20731-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="20731-122">{00067067-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="20731-122">//{00067067-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="20731-123">DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0X0, 0X0, 0xc0, 0X0, 0X0, 0X0, 0X0, 0X0, 0X0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="20731-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  

