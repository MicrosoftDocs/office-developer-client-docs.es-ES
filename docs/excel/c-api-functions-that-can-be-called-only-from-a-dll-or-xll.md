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
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7935d86d1c0a460bcbec85157429d99242a73620
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815528"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a><span data-ttu-id="454d8-104">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="454d8-104">C API Functions That Can Be Called Only from a DLL or XLL</span></span>

<span data-ttu-id="454d8-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="454d8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="454d8-106">La API de C proporciona funciones de devolución de llamada de Microsoft Excel 15 que sólo se pueden llamar mediante la **Excel4**, **Excel4v**, **Excel12**o funciones **Excel12v** (o por una de estas funciones indirectamente utilizando las funciones de Framework **Excel **o **Excel12f**).</span><span class="sxs-lookup"><span data-stu-id="454d8-106">The C API provides 15 Microsoft Excel callback functions that can only be called by using the **Excel4**, **Excel4v**, **Excel12**, or **Excel12v** functions (or by one of these functions indirectly using the Framework functions **Excel** or **Excel12f**).</span></span> <span data-ttu-id="454d8-107">Esto significa que sólo se pueden llamar desde una DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="454d8-107">This means they can only be called from a DLL or XLL.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="454d8-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="454d8-108">In this section</span></span>

[<span data-ttu-id="454d8-109">xlAbort</span><span class="sxs-lookup"><span data-stu-id="454d8-109">xlAbort</span></span>](xlabort.md)
  
[<span data-ttu-id="454d8-110">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="454d8-110">xlAsyncReturn</span></span>](xlasyncreturn.md)
  
[<span data-ttu-id="454d8-111">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="454d8-111">xlCoerce</span></span>](xlcoerce.md)
  
[<span data-ttu-id="454d8-112">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="454d8-112">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
  
[<span data-ttu-id="454d8-113">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="454d8-113">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md)
  
[<span data-ttu-id="454d8-114">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="454d8-114">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md)
  
[<span data-ttu-id="454d8-115">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="454d8-115">xlEventRegister</span></span>](xleventregister.md)
  
[<span data-ttu-id="454d8-116">xlFree</span><span class="sxs-lookup"><span data-stu-id="454d8-116">xlFree</span></span>](xlfree.md)
  
[<span data-ttu-id="454d8-117">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="454d8-117">xlGetBinaryName</span></span>](xlgetbinaryname.md)
  
[<span data-ttu-id="454d8-118">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="454d8-118">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="454d8-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="454d8-119">xlGetInst</span></span>](xlgetinst.md)
  
[<span data-ttu-id="454d8-120">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="454d8-120">xlGetInstPtr</span></span>](xlgetinstptr.md)
  
[<span data-ttu-id="454d8-121">xlGetName</span><span class="sxs-lookup"><span data-stu-id="454d8-121">xlGetName</span></span>](xlgetname.md)
  
[<span data-ttu-id="454d8-122">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="454d8-122">xlRunningOnCluster</span></span>](xlrunningoncluster.md)
  
[<span data-ttu-id="454d8-123">xlSet</span><span class="sxs-lookup"><span data-stu-id="454d8-123">xlSet</span></span>](xlset.md)
  
[<span data-ttu-id="454d8-124">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="454d8-124">xlSheetId</span></span>](xlsheetid.md)
  
[<span data-ttu-id="454d8-125">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="454d8-125">xlSheetNm</span></span>](xlsheetnm.md)
  
[<span data-ttu-id="454d8-126">xlStack</span><span class="sxs-lookup"><span data-stu-id="454d8-126">xlStack</span></span>](xlstack.md)
  
[<span data-ttu-id="454d8-127">xlUDF</span><span class="sxs-lookup"><span data-stu-id="454d8-127">xlUDF</span></span>](xludf.md)
  
## <a name="see-also"></a><span data-ttu-id="454d8-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="454d8-128">See also</span></span>



[<span data-ttu-id="454d8-129">Devoluci�n de llamada de API de C funciona Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="454d8-129">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)

