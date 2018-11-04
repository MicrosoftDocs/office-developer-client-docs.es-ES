---
title: Supports (método, ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4aa04cf3d04b71e0a84279bfc5340e7ee326de48
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949631"
---
# <a name="supports-method-ado"></a><span data-ttu-id="bc21b-102">Supports (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="bc21b-102">Supports method (ADO)</span></span>

<span data-ttu-id="bc21b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc21b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc21b-104">Determina si el objeto [Recordset](recordset-object-ado.md) especificado admite un determinado tipo de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="bc21b-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc21b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc21b-105">Syntax</span></span>

<span data-ttu-id="bc21b-106">*booleano* = *conjunto de registros*. Admite (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="bc21b-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="bc21b-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc21b-107">Return value</span></span>

<span data-ttu-id="bc21b-108">Devuelve un valor **booleano** que indica si el proveedor admite todas las características identificadas por el argumento *CursorOptions* .</span><span class="sxs-lookup"><span data-stu-id="bc21b-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc21b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc21b-109">Parameters</span></span>

|<span data-ttu-id="bc21b-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bc21b-110">Parameter</span></span>|<span data-ttu-id="bc21b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc21b-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="bc21b-112">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="bc21b-112">*CursorOptions*</span></span> |<span data-ttu-id="bc21b-113">Expresión de tipo **Long** formada por uno o varios valores de [CursorOptionEnum](cursoroptionenum.md).</span><span class="sxs-lookup"><span data-stu-id="bc21b-113">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bc21b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc21b-114">Remarks</span></span>

<span data-ttu-id="bc21b-p101">Use el método **Supports** para determinar los tipos de funcionalidad compatibles con un objeto **Recordset**. Si el objeto **Recordset** es compatible con las características cuyas correspondientes constantes están en *CursorOptions*, el método **Supports** devuelve el valor **True**. En caso contrario, devuelve **False**.</span><span class="sxs-lookup"><span data-stu-id="bc21b-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <span data-ttu-id="bc21b-p102">[!NOTA] Si bien el método **Supports** devuelve **True** para una determinada funcionalidad, esto no garantiza que el proveedor tenga disponible la característica en todas las circunstancias. El método **Supports** devuelve simplemente un valor que indica si el proveedor admite la funcionalidad especificada, suponiendo que se cumplen ciertas condiciones. Por ejemplo, puede que el método **Supports** indique que un objeto **Recordset** admita actualizaciones, aun cuando el cursor esté basado en una combinación de varias tablas, en las que algunas de las columnas no son actualizables.</span><span class="sxs-lookup"><span data-stu-id="bc21b-p102">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the **Supports** method may indicate that a **Recordset** object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span>


