---
title: ParentRow (propiedad, ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06bb1110dfa7e7a055fa6cd863dcd2cc17f3f585
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950156"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="a7fd9-102">ParentRow (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="a7fd9-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="a7fd9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7fd9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a7fd9-104">Establece el contenedor de un objeto **Row** de OLE DB en un objeto **ADORecordConstruction**, de modo que la página origen de la fila se convierta en un objeto **Record** de ADO.</span><span class="sxs-lookup"><span data-stu-id="a7fd9-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="a7fd9-105">Sólo escritura.</span><span class="sxs-lookup"><span data-stu-id="a7fd9-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7fd9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7fd9-106">Syntax</span></span>

<span data-ttu-id="a7fd9-107">Poner HRESULT\_ParentRow (\[en\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="a7fd9-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="a7fd9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7fd9-108">Parameters</span></span>

|<span data-ttu-id="a7fd9-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a7fd9-109">Parameter</span></span>|<span data-ttu-id="a7fd9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7fd9-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a7fd9-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="a7fd9-111">*pParent*</span></span> |<span data-ttu-id="a7fd9-112">Contenedor de una fila.</span><span class="sxs-lookup"><span data-stu-id="a7fd9-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="a7fd9-113">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a7fd9-113">Return values</span></span>

<span data-ttu-id="a7fd9-114">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="a7fd9-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a7fd9-115">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="a7fd9-115">Applies to</span></span>

[<span data-ttu-id="a7fd9-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="a7fd9-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

