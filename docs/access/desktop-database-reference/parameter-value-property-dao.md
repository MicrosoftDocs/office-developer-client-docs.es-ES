---
title: Propiedad Parameter. Value (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4e7f3976b934c407a038f321953259fd63a6f60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287996"
---
# <a name="parametervalue-property-dao"></a><span data-ttu-id="5e889-102">Propiedad Parameter. Value (DAO)</span><span class="sxs-lookup"><span data-stu-id="5e889-102">Parameter.Value property (DAO)</span></span>

<span data-ttu-id="5e889-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e889-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5e889-104">Establece o devuelve el valor de un objeto.</span><span class="sxs-lookup"><span data-stu-id="5e889-104">Sets or returns the value of an object.</span></span> <span data-ttu-id="5e889-105">**Variante** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5e889-105">Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e889-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e889-106">Syntax</span></span>

<span data-ttu-id="5e889-107">*expresión* . Value</span><span class="sxs-lookup"><span data-stu-id="5e889-107">*expression* .Value</span></span>

<span data-ttu-id="5e889-108">*expresión* Variable que representa un objeto **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="5e889-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e889-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e889-109">Remarks</span></span>

<span data-ttu-id="5e889-110">La configuración o el valor devuelto es un tipo de datos Variant que evalúa en un valor apropiado para el tipo de datos, como el especificado por la propiedad de un objeto **Type**.</span><span class="sxs-lookup"><span data-stu-id="5e889-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="5e889-111">En general, la propiedad **Value** se usa para recuperar y alterar los datos en los objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5e889-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="5e889-p102">La propiedad **Value** es la propiedad predeterminada de los objetos **Field**, **Parameter** y **Property**. Por tanto, puede establecer o devolver el valor de uno de esos objetos al referirse a ellos directamente en vez de especificar la propiedad **Value**.</span><span class="sxs-lookup"><span data-stu-id="5e889-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="5e889-114">Si intenta establecer o devolver la propiedad **Value** en un contexto poco apropiado (por ejemplo, la propiedad **Value** de un objeto **Field** en la colección **Fields** de un objeto **TableDef**) se producirá un error capturable.</span><span class="sxs-lookup"><span data-stu-id="5e889-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>

> [!NOTE]
> <span data-ttu-id="5e889-115">Cuando se lean valores decimales de una base de datos de Microsoft SQL Server, se les dará formato con notación científica a través de un área de trabajo de Microsoft Access, pero aparecerán como valores decimales normales a través de un área de trabajo de ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="5e889-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


