---
title: Supports (método, ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceeab22cda05738fdcec090acb5b4a2d6fc88a5b
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604263"
---
# <a name="supports-method-ado"></a><span data-ttu-id="bc40e-102">Supports (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="bc40e-102">Supports Method (ADO)</span></span>


<span data-ttu-id="bc40e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc40e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bc40e-104">Determina si el objeto [Recordset](recordset-object-ado.md) especificado admite un determinado tipo de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="bc40e-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc40e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc40e-105">Syntax</span></span>

<span data-ttu-id="bc40e-106">*booleano* = *conjunto de registros*. Admite (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="bc40e-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

<span data-ttu-id="bc40e-107"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="bc40e-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="bc40e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc40e-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="bc40e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc40e-109">Return value</span></span>
>>>>>>> <span data-ttu-id="bc40e-110">master</span><span class="sxs-lookup"><span data-stu-id="bc40e-110">master</span></span>

<span data-ttu-id="bc40e-111">Devuelve un valor **booleano** que indica si el proveedor admite todas las características identificadas por el argumento *CursorOptions* .</span><span class="sxs-lookup"><span data-stu-id="bc40e-111">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc40e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc40e-112">Parameters</span></span>

  - <span data-ttu-id="bc40e-113">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="bc40e-113">*CursorOptions*</span></span>

  - <span data-ttu-id="bc40e-114">Expresión de tipo **Long** formada por uno o varios valores de [CursorOptionEnum](cursoroptionenum.md).</span><span class="sxs-lookup"><span data-stu-id="bc40e-114">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc40e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc40e-115">Remarks</span></span>

<span data-ttu-id="bc40e-p101">Use el método **Supports** para determinar los tipos de funcionalidad compatibles con un objeto **Recordset**. Si el objeto **Recordset** es compatible con las características cuyas correspondientes constantes están en *CursorOptions*, el método **Supports** devuelve el valor **True**. En caso contrario, devuelve **False**.</span><span class="sxs-lookup"><span data-stu-id="bc40e-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bc40e-p102">[!NOTA] Si bien el método <STRONG>Supports</STRONG> devuelve <STRONG>True</STRONG> para una determinada funcionalidad, esto no garantiza que el proveedor tenga disponible la característica en todas las circunstancias. El método <STRONG>Supports</STRONG> devuelve simplemente un valor que indica si el proveedor admite la funcionalidad especificada, suponiendo que se cumplen ciertas condiciones. Por ejemplo, puede que el método <STRONG>Supports</STRONG> indique que un objeto <STRONG>Recordset</STRONG> admita actualizaciones, aun cuando el cursor esté basado en una combinación de varias tablas, en las que algunas de las columnas no son actualizables.</span><span class="sxs-lookup"><span data-stu-id="bc40e-p102">Although the <STRONG>Supports</STRONG> method may return <STRONG>True</STRONG> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The <STRONG>Supports</STRONG> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the <STRONG>Supports</STRONG> method may indicate that a <STRONG>Recordset</STRONG> object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span></P>


