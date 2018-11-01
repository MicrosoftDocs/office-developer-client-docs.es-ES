---
title: Fila (propiedad) - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7578a00719946450e840080c21284784a27be170
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870950"
---
# <a name="row-property-ado"></a><span data-ttu-id="1cb56-102">Row (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="1cb56-102">Row property (ADO)</span></span>


<span data-ttu-id="1cb56-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cb56-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="1cb56-104">Obtiene o establece un objeto **Row** de OLE DB desde o en un objeto **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="1cb56-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="1cb56-105">Al usar **colocar\_fila** para establecer un objeto **Row** , una fila se convierta en un objeto **Record** de ADO.</span><span class="sxs-lookup"><span data-stu-id="1cb56-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="1cb56-106">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1cb56-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cb56-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cb56-107">Syntax</span></span>

<span data-ttu-id="1cb56-108">Get HRESULT\_fila (\[out, retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="1cb56-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="1cb56-109">Poner HRESULT\_fila (\[en\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="1cb56-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="1cb56-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cb56-110">Parameters</span></span>

  - <span data-ttu-id="1cb56-111">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="1cb56-111">*ppRow*</span></span>

  - <span data-ttu-id="1cb56-112">Puntero a un objeto **Row** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1cb56-112">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="1cb56-113">*PRow*</span><span class="sxs-lookup"><span data-stu-id="1cb56-113">*PRow*</span></span>

  - <span data-ttu-id="1cb56-114">Un objeto **Row** de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1cb56-114">An OLE DB **Row** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="1cb56-115">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="1cb56-115">Return values</span></span>

<span data-ttu-id="1cb56-116">Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.</span><span class="sxs-lookup"><span data-stu-id="1cb56-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1cb56-117">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="1cb56-117">Applies To</span></span>

[<span data-ttu-id="1cb56-118">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="1cb56-118">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

