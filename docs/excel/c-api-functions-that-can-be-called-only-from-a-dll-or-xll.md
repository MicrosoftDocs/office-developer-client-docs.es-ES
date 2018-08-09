---
title: Funciones de la API de C que se pueden llamar solo desde una DLL o XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funciones [excel 2007], llama a api de c desde dll o xll
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7935d86d1c0a460bcbec85157429d99242a73620
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815528"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a><span data-ttu-id="badeb-104">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="badeb-104">C API Functions That Can Be Called Only from a DLL or XLL</span></span>

<span data-ttu-id="badeb-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="badeb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="badeb-106">La API de C proporciona funciones de devolución de llamada de Microsoft Excel 15 que sólo se pueden llamar mediante la **Excel4**, **Excel4v**, **Excel12**o funciones **Excel12v** (o por una de estas funciones indirectamente utilizando las funciones de Framework **Excel **o **Excel12f**).</span><span class="sxs-lookup"><span data-stu-id="badeb-106">The C API provides 15 Microsoft Excel callback functions that can only be called by using the **Excel4**, **Excel4v**, **Excel12**, or **Excel12v** functions (or by one of these functions indirectly using the Framework functions **Excel** or **Excel12f**).</span></span> <span data-ttu-id="badeb-107">Esto significa que sólo se pueden llamar desde una DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="badeb-107">This means they can only be called from a DLL or XLL.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="badeb-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="badeb-108">In this section</span></span>

[<span data-ttu-id="badeb-109">xlAbort</span><span class="sxs-lookup"><span data-stu-id="badeb-109">xlAbort</span></span>](xlabort.md)
  
[<span data-ttu-id="badeb-110">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="badeb-110">xlAsyncReturn</span></span>](xlasyncreturn.md)
  
[<span data-ttu-id="badeb-111">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="badeb-111">xlCoerce</span></span>](xlcoerce.md)
  
[<span data-ttu-id="badeb-112">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="badeb-112">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
  
[<span data-ttu-id="badeb-113">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="badeb-113">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md)
  
[<span data-ttu-id="badeb-114">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="badeb-114">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md)
  
[<span data-ttu-id="badeb-115">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="badeb-115">xlEventRegister</span></span>](xleventregister.md)
  
[<span data-ttu-id="badeb-116">xlFree</span><span class="sxs-lookup"><span data-stu-id="badeb-116">xlFree</span></span>](xlfree.md)
  
[<span data-ttu-id="badeb-117">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="badeb-117">xlGetBinaryName</span></span>](xlgetbinaryname.md)
  
[<span data-ttu-id="badeb-118">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="badeb-118">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="badeb-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="badeb-119">xlGetInst</span></span>](xlgetinst.md)
  
[<span data-ttu-id="badeb-120">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="badeb-120">xlGetInstPtr</span></span>](xlgetinstptr.md)
  
[<span data-ttu-id="badeb-121">xlGetName</span><span class="sxs-lookup"><span data-stu-id="badeb-121">xlGetName</span></span>](xlgetname.md)
  
[<span data-ttu-id="badeb-122">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="badeb-122">xlRunningOnCluster</span></span>](xlrunningoncluster.md)
  
[<span data-ttu-id="badeb-123">xlSet</span><span class="sxs-lookup"><span data-stu-id="badeb-123">xlSet</span></span>](xlset.md)
  
[<span data-ttu-id="badeb-124">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="badeb-124">xlSheetId</span></span>](xlsheetid.md)
  
[<span data-ttu-id="badeb-125">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="badeb-125">xlSheetNm</span></span>](xlsheetnm.md)
  
[<span data-ttu-id="badeb-126">xlStack</span><span class="sxs-lookup"><span data-stu-id="badeb-126">xlStack</span></span>](xlstack.md)
  
[<span data-ttu-id="badeb-127">xlUDF</span><span class="sxs-lookup"><span data-stu-id="badeb-127">xlUDF</span></span>](xludf.md)
  
## <a name="see-also"></a><span data-ttu-id="badeb-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="badeb-128">See also</span></span>



[<span data-ttu-id="badeb-129">Funciones de devolución de llamada de API de C de Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="badeb-129">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)

