---
title: Rowset (propiedad, ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306744"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="c9e98-102">Rowset (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="c9e98-102">Rowset property (ADO)</span></span>

<span data-ttu-id="c9e98-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9e98-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9e98-104">Obtiene o establece un objeto **Rowset** de OLE DB desde o en un objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="c9e98-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="c9e98-105">Cuando se utiliza Put\_Rowset, el conjunto de filas se convierte en un objeto **Recordset** de ADO.</span><span class="sxs-lookup"><span data-stu-id="c9e98-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="c9e98-106">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c9e98-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9e98-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9e98-107">Syntax</span></span>

<span data-ttu-id="c9e98-108">HRESULT Get\_Rowset (\[out, retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="c9e98-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="c9e98-109">HRESULT Put\_Rowset (\[en\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="c9e98-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="c9e98-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9e98-110">Parameters</span></span>

|<span data-ttu-id="c9e98-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9e98-111">Parameter</span></span>|<span data-ttu-id="c9e98-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9e98-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c9e98-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="c9e98-113">*ppRowset*</span></span> |<span data-ttu-id="c9e98-114">Puntero a un objeto **Rowset** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c9e98-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="c9e98-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="c9e98-115">*PRowset*</span></span> |<span data-ttu-id="c9e98-116">Un objeto **Rowset** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c9e98-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="c9e98-117">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="c9e98-117">Return values</span></span>

<span data-ttu-id="c9e98-118">Este método de propiedad devuelve los valores HRESULT estándar, incluidos\_los errores S\_OK y e.</span><span class="sxs-lookup"><span data-stu-id="c9e98-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c9e98-119">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="c9e98-119">Applies to</span></span>

[<span data-ttu-id="c9e98-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="c9e98-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

