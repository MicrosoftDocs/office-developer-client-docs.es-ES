---
title: Fila (propiedad) - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715007"
---
# <a name="row-property-ado"></a><span data-ttu-id="b0323-102">Row (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="b0323-102">Row property (ADO)</span></span>

<span data-ttu-id="b0323-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0323-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0323-104">Obtiene o establece un objeto **Row** de OLE DB desde o en un objeto **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="b0323-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="b0323-105">Al usar **colocar\_fila** para establecer un objeto **Row** , una fila se convierta en un objeto **Record** de ADO.</span><span class="sxs-lookup"><span data-stu-id="b0323-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="b0323-106">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b0323-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0323-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0323-107">Syntax</span></span>

<span data-ttu-id="b0323-108">Get HRESULT\_fila (\[out, retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="b0323-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="b0323-109">Poner HRESULT\_fila (\[en\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="b0323-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="b0323-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0323-110">Parameters</span></span>

|<span data-ttu-id="b0323-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b0323-111">Parameter</span></span>|<span data-ttu-id="b0323-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0323-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b0323-113">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="b0323-113">*ppRow*</span></span> |<span data-ttu-id="b0323-114">Puntero a un objeto **Row** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="b0323-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="b0323-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="b0323-115">*PRow*</span></span> |<span data-ttu-id="b0323-116">Un objeto **Row** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="b0323-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="b0323-117">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b0323-117">Return values</span></span>

<span data-ttu-id="b0323-118">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="b0323-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b0323-119">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="b0323-119">Applies to</span></span>

[<span data-ttu-id="b0323-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="b0323-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

