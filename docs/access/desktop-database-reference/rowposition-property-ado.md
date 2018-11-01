---
title: RowPosition (propiedad, ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f83d1b113b29be06ffded5263791d3db3068f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869074"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="43caa-102">RowPosition (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="43caa-102">RowPosition property (ADO)</span></span>


<span data-ttu-id="43caa-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="43caa-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="43caa-104">Obtiene o establece un objeto **RowPosition** de OLE DB desde o en un objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="43caa-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="43caa-105">Al usar **colocar\_RowPosition** para establecer el objeto **RowPosition** , el objeto **Recordset** resultante utiliza el objeto **RowPosition** para determinar la fila actual.</span><span class="sxs-lookup"><span data-stu-id="43caa-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="43caa-106">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="43caa-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="43caa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43caa-107">Syntax</span></span>

<span data-ttu-id="43caa-108">Get HRESULT\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="43caa-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="43caa-109">Poner HRESULT\_RowPosition (\[en\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="43caa-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="43caa-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43caa-110">Parameters</span></span>

  - <span data-ttu-id="43caa-111">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="43caa-111">*ppRowPos*</span></span>

  - <span data-ttu-id="43caa-112">Puntero a un objeto **RowPosition** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="43caa-112">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="43caa-113">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="43caa-113">*PRowPos*</span></span>

  - <span data-ttu-id="43caa-114">Un objeto **RowPosition** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="43caa-114">An OLE DB **RowPosition** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="43caa-115">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="43caa-115">Return values</span></span>

<span data-ttu-id="43caa-116">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="43caa-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="43caa-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43caa-117">Remarks</span></span>

<span data-ttu-id="43caa-p102">Cuando se establece esta propiedad, si el objeto **Rowset** del objeto **RowPosition** es diferente al objeto **Rowset** del objeto **Recordset**, el primero sobrescribe al segundo. El mismo comportamiento se aplica al **capítulo** actual de **RowPosition**.</span><span class="sxs-lookup"><span data-stu-id="43caa-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="43caa-120">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="43caa-120">Applies To</span></span>

[<span data-ttu-id="43caa-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="43caa-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

