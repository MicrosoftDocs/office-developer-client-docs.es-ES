---
title: Rowset (propiedad, ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d5979cb42e2ed4a979dc07016a4bb02b8097994
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949792"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="360cd-102">Rowset (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="360cd-102">Rowset property (ADO)</span></span>

<span data-ttu-id="360cd-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="360cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="360cd-104">Obtiene o establece un objeto **Rowset** de OLE DB desde o en un objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="360cd-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="360cd-105">Cuando use put\_conjunto de filas, el conjunto de filas se convierte en un objeto **Recordset** de ADO.</span><span class="sxs-lookup"><span data-stu-id="360cd-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="360cd-106">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="360cd-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="360cd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="360cd-107">Syntax</span></span>

<span data-ttu-id="360cd-108">Get HRESULT\_conjunto de filas (\[out, retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="360cd-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="360cd-109">Poner HRESULT\_conjunto de filas (\[en\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="360cd-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="360cd-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="360cd-110">Parameters</span></span>

|<span data-ttu-id="360cd-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="360cd-111">Parameter</span></span>|<span data-ttu-id="360cd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="360cd-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="360cd-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="360cd-113">*ppRowset*</span></span> |<span data-ttu-id="360cd-114">Puntero a un objeto **Rowset** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="360cd-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="360cd-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="360cd-115">*PRowset*</span></span> |<span data-ttu-id="360cd-116">Un objeto **Rowset** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="360cd-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="360cd-117">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="360cd-117">Return values</span></span>

<span data-ttu-id="360cd-118">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="360cd-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="360cd-119">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="360cd-119">Applies to</span></span>

[<span data-ttu-id="360cd-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="360cd-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

