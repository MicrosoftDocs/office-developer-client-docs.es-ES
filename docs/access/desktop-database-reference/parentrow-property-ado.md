---
title: Propiedad ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287741"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="d96c8-102">Propiedad ParentRow (ADO)</span><span class="sxs-lookup"><span data-stu-id="d96c8-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="d96c8-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d96c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d96c8-104">Establece el contenedor de un objeto **Row** de OLE DB en un objeto **ADORecordConstruction**, de modo que la página origen de la fila se convierta en un objeto **Record** de ADO.</span><span class="sxs-lookup"><span data-stu-id="d96c8-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="d96c8-105">Sólo escritura.</span><span class="sxs-lookup"><span data-stu-id="d96c8-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d96c8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d96c8-106">Syntax</span></span>

<span data-ttu-id="d96c8-107">HRESULT put \_ ParentRow( \[ in \] IUnknown \* pParent);</span><span class="sxs-lookup"><span data-stu-id="d96c8-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="d96c8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d96c8-108">Parameters</span></span>

|<span data-ttu-id="d96c8-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d96c8-109">Parameter</span></span>|<span data-ttu-id="d96c8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d96c8-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d96c8-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="d96c8-111">*pParent*</span></span> |<span data-ttu-id="d96c8-112">Contenedor de una fila.</span><span class="sxs-lookup"><span data-stu-id="d96c8-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="d96c8-113">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d96c8-113">Return values</span></span>

<span data-ttu-id="d96c8-114">Este método de propiedad devuelve los valores HRESULT estándar, incluidos S \_ OK y E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="d96c8-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d96c8-115">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="d96c8-115">Applies to</span></span>

[<span data-ttu-id="d96c8-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="d96c8-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

