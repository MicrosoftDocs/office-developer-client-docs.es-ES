---
title: RowPosition (propiedad, ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306863"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="98d1d-102">RowPosition (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="98d1d-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="98d1d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98d1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98d1d-104">Obtiene o establece un objeto **RowPosition** de OLE DB desde o en un objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="98d1d-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="98d1d-105">Cuando se utiliza **Put\_RowPosition** para establecer el objeto **RowPosition** , el objeto **Recordset** resultante utiliza el objeto **rowposition** para determinar la fila actual.</span><span class="sxs-lookup"><span data-stu-id="98d1d-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="98d1d-106">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="98d1d-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d1d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98d1d-107">Syntax</span></span>

<span data-ttu-id="98d1d-108">HRESULT Get\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="98d1d-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="98d1d-109">HRESULT Put\_RowPosition (\[en\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="98d1d-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="98d1d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98d1d-110">Parameters</span></span>

|<span data-ttu-id="98d1d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="98d1d-111">Parameter</span></span>|<span data-ttu-id="98d1d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="98d1d-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="98d1d-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="98d1d-113">*ppRowPos*</span></span> |<span data-ttu-id="98d1d-114">Puntero a un objeto **RowPosition** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="98d1d-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="98d1d-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="98d1d-115">*PRowPos*</span></span> |<span data-ttu-id="98d1d-116">Un objeto **RowPosition** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="98d1d-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="98d1d-117">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="98d1d-117">Return values</span></span>

<span data-ttu-id="98d1d-118">Este método de propiedad devuelve los valores HRESULT estándar, incluidos\_los errores S\_OK y e.</span><span class="sxs-lookup"><span data-stu-id="98d1d-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="98d1d-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98d1d-119">Remarks</span></span>

<span data-ttu-id="98d1d-p102">Cuando se establece esta propiedad, si el objeto **Rowset** del objeto **RowPosition** es diferente al objeto **Rowset** del objeto **Recordset**, el primero sobrescribe al segundo. El mismo comportamiento se aplica al **capítulo** actual de **RowPosition**.</span><span class="sxs-lookup"><span data-stu-id="98d1d-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="98d1d-122">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="98d1d-122">Applies to</span></span>

[<span data-ttu-id="98d1d-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="98d1d-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

