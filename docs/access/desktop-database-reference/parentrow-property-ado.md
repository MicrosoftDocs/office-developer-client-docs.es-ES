---
title: ParentRow (propiedad, ADO)
TOCTitle: ParentRow Property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 834dcaed7d1acdcf66410584436e2ccee8c91c56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486809"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="d4eff-102">ParentRow (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="d4eff-102">ParentRow Property (ADO)</span></span>


<span data-ttu-id="d4eff-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d4eff-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="d4eff-104">Establece el contenedor de un objeto **Row** de OLE DB en un objeto **ADORecordConstruction**, de modo que la página origen de la fila se convierta en un objeto **Record** de ADO.</span><span class="sxs-lookup"><span data-stu-id="d4eff-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="d4eff-105">Sólo escritura.</span><span class="sxs-lookup"><span data-stu-id="d4eff-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4eff-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4eff-106">Syntax</span></span>

<span data-ttu-id="d4eff-107">Poner HRESULT\_ParentRow (\[en\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="d4eff-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="d4eff-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4eff-108">Parameters</span></span>

  - <span data-ttu-id="d4eff-109">*pParent*</span><span class="sxs-lookup"><span data-stu-id="d4eff-109">*pParent*</span></span>

  - <span data-ttu-id="d4eff-110">Contenedor de una fila.</span><span class="sxs-lookup"><span data-stu-id="d4eff-110">A container of a row.</span></span>

## <a name="return-values"></a><span data-ttu-id="d4eff-111">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d4eff-111">Return Values</span></span>

<span data-ttu-id="d4eff-112">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="d4eff-112">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d4eff-113">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="d4eff-113">Applies To</span></span>

[<span data-ttu-id="d4eff-114">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="d4eff-114">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

