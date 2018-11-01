---
title: Parameter.Value Property (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21aef110b73b851c83af95fbc7cbf1de47d10747
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870012"
---
# <a name="parametervalue-property-dao"></a><span data-ttu-id="07ee4-102">Parameter.Value Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="07ee4-102">Parameter.Value Property (DAO)</span></span>


<span data-ttu-id="07ee4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07ee4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07ee4-p101">Establece o devuelve el valor de un objeto. **Variant** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="07ee4-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="07ee4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07ee4-106">Syntax</span></span>

<span data-ttu-id="07ee4-107">*expresión* . Valor</span><span class="sxs-lookup"><span data-stu-id="07ee4-107">*expression* .Value</span></span>

<span data-ttu-id="07ee4-108">*expresión* Variable que representa un objeto **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="07ee4-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="07ee4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07ee4-109">Remarks</span></span>

<span data-ttu-id="07ee4-110">La configuración o el valor devuelto es un tipo de datos Variant que da como resultado un valor apropiado para el tipo de datos, tal como especifica la propiedad **Type** de un objeto.</span><span class="sxs-lookup"><span data-stu-id="07ee4-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="07ee4-111">En general, la propiedad **Value** se usa para recuperar y modificar datos en objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="07ee4-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="07ee4-p102">La propiedad **Value** es la propiedad predeterminada de los objetos **Field**, **Parameter** y **Property**. Por lo tanto, puede hacer que se establezca o devuelva el valor de uno de estos objetos haciendo referencia a ellos directamente en lugar de especificar la propiedad **Value**.</span><span class="sxs-lookup"><span data-stu-id="07ee4-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="07ee4-114">Si intenta que se establezca o devuelva la propiedad **Value** en un contexto no apropiado (por ejemplo, la propiedad **Value** de un objeto **Field** de la colección **Fields** de un objeto **TableDef**) se producirá un error capturable.</span><span class="sxs-lookup"><span data-stu-id="07ee4-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="07ee4-115">Cuando se lean valores decimales de una base de datos de Microsoft SQL Server, se les dará formato con notación científica a través de un área de trabajo de Microsoft Access, pero aparecerán como valores decimales normales a través de un área de trabajo de ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="07ee4-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span></P>


