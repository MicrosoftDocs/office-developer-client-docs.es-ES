---
title: Supports (método, ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ac3d3e1be9ff703a0e11435b776eabeb15b30eb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920630"
---
# <a name="supports-method-ado"></a><span data-ttu-id="ba4c0-102">Supports (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="ba4c0-102">Supports method (ADO)</span></span>


<span data-ttu-id="ba4c0-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba4c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba4c0-104">Determina si el objeto [Recordset](recordset-object-ado.md) especificado admite un determinado tipo de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba4c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba4c0-105">Syntax</span></span>

<span data-ttu-id="ba4c0-106">*booleano* = *conjunto de registros*. Admite (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="ba4c0-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="ba4c0-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba4c0-107">Return value</span></span>

<span data-ttu-id="ba4c0-108">Devuelve un valor **booleano** que indica si el proveedor admite todas las características identificadas por el argumento *CursorOptions* .</span><span class="sxs-lookup"><span data-stu-id="ba4c0-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba4c0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba4c0-109">Parameters</span></span>

  - <span data-ttu-id="ba4c0-110">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="ba4c0-110">*CursorOptions*</span></span>

  - <span data-ttu-id="ba4c0-111">Expresión de tipo **Long** formada por uno o varios valores de [CursorOptionEnum](cursoroptionenum.md).</span><span class="sxs-lookup"><span data-stu-id="ba4c0-111">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba4c0-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba4c0-112">Remarks</span></span>

<span data-ttu-id="ba4c0-p101">Use el método **Supports** para determinar los tipos de funcionalidad compatibles con un objeto **Recordset**. Si el objeto **Recordset** es compatible con las características cuyas correspondientes constantes están en *CursorOptions*, el método **Supports** devuelve el valor **True**. En caso contrario, devuelve **False**.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ba4c0-p102">[!NOTA] Si bien el método <STRONG>Supports</STRONG> devuelve <STRONG>True</STRONG> para una determinada funcionalidad, esto no garantiza que el proveedor tenga disponible la característica en todas las circunstancias. El método <STRONG>Supports</STRONG> devuelve simplemente un valor que indica si el proveedor admite la funcionalidad especificada, suponiendo que se cumplen ciertas condiciones. Por ejemplo, puede que el método <STRONG>Supports</STRONG> indique que un objeto <STRONG>Recordset</STRONG> admita actualizaciones, aun cuando el cursor esté basado en una combinación de varias tablas, en las que algunas de las columnas no son actualizables.</span><span class="sxs-lookup"><span data-stu-id="ba4c0-p102">Although the <STRONG>Supports</STRONG> method may return <STRONG>True</STRONG> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The <STRONG>Supports</STRONG> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the <STRONG>Supports</STRONG> method may indicate that a <STRONG>Recordset</STRONG> object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span></P>


