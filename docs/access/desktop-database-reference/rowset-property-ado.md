---
title: Rowset (propiedad, ADO)
TOCTitle: Rowset Property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95a33fb3d24e5cdbf608d268781be0dd536fa315
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485042"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="15ebe-102">Rowset (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="15ebe-102">Rowset Property (ADO)</span></span>


<span data-ttu-id="15ebe-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="15ebe-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="15ebe-104">Obtiene o establece un objeto **Rowset** de OLE DB desde o en un objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="15ebe-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="15ebe-105">Cuando use put\_conjunto de filas, el conjunto de filas se convierte en un objeto **Recordset** de ADO.</span><span class="sxs-lookup"><span data-stu-id="15ebe-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="15ebe-106">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="15ebe-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ebe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15ebe-107">Syntax</span></span>

<span data-ttu-id="15ebe-108">Get HRESULT\_conjunto de filas (\[out, retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="15ebe-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="15ebe-109">Poner HRESULT\_conjunto de filas (\[en\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="15ebe-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="15ebe-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15ebe-110">Parameters</span></span>

  - <span data-ttu-id="15ebe-111">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="15ebe-111">*ppRowset*</span></span>

  - <span data-ttu-id="15ebe-112">Puntero a un objeto **Rowset** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="15ebe-112">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="15ebe-113">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="15ebe-113">*PRowset*</span></span>

  - <span data-ttu-id="15ebe-114">Un objeto **Rowset** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="15ebe-114">An OLE DB **Rowset** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="15ebe-115">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="15ebe-115">Return Values</span></span>

<span data-ttu-id="15ebe-116">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="15ebe-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="15ebe-117">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="15ebe-117">Applies To</span></span>

[<span data-ttu-id="15ebe-118">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="15ebe-118">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

