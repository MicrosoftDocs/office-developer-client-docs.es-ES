---
title: RowPosition (propiedad, ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0adb1cdf9ce7b096d7b80b86a89a819d5789b60b
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949386"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="f0fc2-102">RowPosition (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="f0fc2-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="f0fc2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0fc2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0fc2-104">Obtiene o establece un objeto **RowPosition** de OLE DB desde o en un objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="f0fc2-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="f0fc2-105">Al usar **colocar\_RowPosition** para establecer el objeto **RowPosition** , el objeto **Recordset** resultante utiliza el objeto **RowPosition** para determinar la fila actual.</span><span class="sxs-lookup"><span data-stu-id="f0fc2-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="f0fc2-106">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f0fc2-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0fc2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0fc2-107">Syntax</span></span>

<span data-ttu-id="f0fc2-108">Get HRESULT\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="f0fc2-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="f0fc2-109">Poner HRESULT\_RowPosition (\[en\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="f0fc2-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="f0fc2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0fc2-110">Parameters</span></span>

|<span data-ttu-id="f0fc2-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f0fc2-111">Parameter</span></span>|<span data-ttu-id="f0fc2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0fc2-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f0fc2-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="f0fc2-113">*ppRowPos*</span></span> |<span data-ttu-id="f0fc2-114">Puntero a un objeto **RowPosition** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f0fc2-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="f0fc2-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="f0fc2-115">*PRowPos*</span></span> |<span data-ttu-id="f0fc2-116">Un objeto **RowPosition** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f0fc2-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="f0fc2-117">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f0fc2-117">Return values</span></span>

<span data-ttu-id="f0fc2-118">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="f0fc2-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0fc2-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0fc2-119">Remarks</span></span>

<span data-ttu-id="f0fc2-p102">Cuando se establece esta propiedad, si el objeto **Rowset** del objeto **RowPosition** es diferente al objeto **Rowset** del objeto **Recordset**, el primero sobrescribe al segundo. El mismo comportamiento se aplica al **capítulo** actual de **RowPosition**.</span><span class="sxs-lookup"><span data-stu-id="f0fc2-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f0fc2-122">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="f0fc2-122">Applies to</span></span>

[<span data-ttu-id="f0fc2-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="f0fc2-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

