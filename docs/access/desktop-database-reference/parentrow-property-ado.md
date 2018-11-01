---
title: ParentRow (propiedad, ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28f0d1c7dbc0e062ff133b9f9997f1a737c3262e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872133"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="d813a-102">ParentRow (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="d813a-102">ParentRow property (ADO)</span></span>


<span data-ttu-id="d813a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d813a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="d813a-104">Establece el contenedor de un objeto **Row** de OLE DB en un objeto **ADORecordConstruction**, de modo que la página origen de la fila se convierta en un objeto **Record** de ADO.</span><span class="sxs-lookup"><span data-stu-id="d813a-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="d813a-105">Sólo escritura.</span><span class="sxs-lookup"><span data-stu-id="d813a-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d813a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d813a-106">Syntax</span></span>

<span data-ttu-id="d813a-107">Poner HRESULT\_ParentRow (\[en\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="d813a-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="d813a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d813a-108">Parameters</span></span>

  - <span data-ttu-id="d813a-109">*pParent*</span><span class="sxs-lookup"><span data-stu-id="d813a-109">*pParent*</span></span>

  - <span data-ttu-id="d813a-110">Contenedor de una fila.</span><span class="sxs-lookup"><span data-stu-id="d813a-110">A container of a row.</span></span>

## <a name="return-values"></a><span data-ttu-id="d813a-111">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d813a-111">Return values</span></span>

<span data-ttu-id="d813a-112">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="d813a-112">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d813a-113">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="d813a-113">Applies To</span></span>

[<span data-ttu-id="d813a-114">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="d813a-114">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

