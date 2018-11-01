---
title: Chapter (propiedad, ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5eeb3c6e2e8c7b7f1c0f6e733c1b86545a5e954f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887827"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="c5cd9-102">Chapter (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="c5cd9-102">Chapter property (ADO)</span></span>


<span data-ttu-id="c5cd9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5cd9-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="c5cd9-104">Obtiene o establece un objeto **Chapter** de OLE DB de/en un objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="c5cd9-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="c5cd9-105">Al usar **colocar\_capítulo** para establecer el objeto **Chapter** , un subconjunto de filas se convierte en un objeto **Recordset** de ADO.</span><span class="sxs-lookup"><span data-stu-id="c5cd9-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="c5cd9-106">De este modo, se establece el capítulo actual del objeto **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="c5cd9-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="c5cd9-107">Lectura/Escritura.</span><span class="sxs-lookup"><span data-stu-id="c5cd9-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5cd9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5cd9-108">Syntax</span></span>

<span data-ttu-id="c5cd9-109">Get HRESULT\_capítulo (\[out, retval\] largo\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="c5cd9-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="c5cd9-110">Poner HRESULT\_capítulo (\[en\] lChapter largo);</span><span class="sxs-lookup"><span data-stu-id="c5cd9-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="c5cd9-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5cd9-111">Parameters</span></span>

  - <span data-ttu-id="c5cd9-112">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="c5cd9-112">*plChapter*</span></span>

  - <span data-ttu-id="c5cd9-113">Puntero al controlador de un capítulo.</span><span class="sxs-lookup"><span data-stu-id="c5cd9-113">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="c5cd9-114">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="c5cd9-114">*LChapter*</span></span>

  - <span data-ttu-id="c5cd9-115">Controlador de un capítulo.</span><span class="sxs-lookup"><span data-stu-id="c5cd9-115">Handle of a chapter.</span></span>

## <a name="return-values"></a><span data-ttu-id="c5cd9-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="c5cd9-116">Return values</span></span>

<span data-ttu-id="c5cd9-117">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="c5cd9-117">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c5cd9-118">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="c5cd9-118">Applies To</span></span>

[<span data-ttu-id="c5cd9-119">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="c5cd9-119">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

