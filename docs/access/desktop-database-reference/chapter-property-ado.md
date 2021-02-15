---
title: Propiedad Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296398"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="65ffd-102">Propiedad Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="65ffd-102">Chapter property (ADO)</span></span>

<span data-ttu-id="65ffd-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65ffd-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="65ffd-104">Obtiene o establece un objeto **Chapter** de OLE DB de/en un objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="65ffd-105">Cuando se usa **put \_ Chapter** para establecer el **objeto Chapter,** se convierte un subconjunto de filas en un objeto **Recordset** de ADO.</span><span class="sxs-lookup"><span data-stu-id="65ffd-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="65ffd-106">De este modo, se establece el capítulo actual del objeto **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="65ffd-107">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="65ffd-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ffd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65ffd-108">Syntax</span></span>

<span data-ttu-id="65ffd-109">HRESULT get \_ Chapter( \[ out, retval \] long \* plChapter);</span><span class="sxs-lookup"><span data-stu-id="65ffd-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="65ffd-110">HRESULT put \_ Chapter( \[ in long \] lChapter);</span><span class="sxs-lookup"><span data-stu-id="65ffd-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="65ffd-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65ffd-111">Parameters</span></span>

|<span data-ttu-id="65ffd-112">Parámetro</span><span class="sxs-lookup"><span data-stu-id="65ffd-112">Parameter</span></span>|<span data-ttu-id="65ffd-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="65ffd-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="65ffd-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="65ffd-114">*plChapter*</span></span> |<span data-ttu-id="65ffd-115">Puntero al controlador de un capítulo.</span><span class="sxs-lookup"><span data-stu-id="65ffd-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="65ffd-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="65ffd-116">*LChapter*</span></span> |<span data-ttu-id="65ffd-117">Controlador de un capítulo.</span><span class="sxs-lookup"><span data-stu-id="65ffd-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="65ffd-118">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="65ffd-118">Return values</span></span>

<span data-ttu-id="65ffd-119">Este método de propiedad devuelve los valores HRESULT estándar, incluidos S \_ OK y E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="65ffd-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="65ffd-120">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="65ffd-120">Applies To</span></span>

[<span data-ttu-id="65ffd-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="65ffd-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

