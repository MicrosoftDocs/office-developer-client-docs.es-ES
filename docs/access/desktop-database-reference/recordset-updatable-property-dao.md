---
title: Recordset.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 2d4bdcef-1b10-b542-ce0f-6172c271131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192110(v=office.15)
ms:contentKeyID: 48543968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 77f3c7331e42d0f9a63a0f87330f8acbc49a646b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483775"
---
# <a name="recordsetupdatable-property-dao"></a><span data-ttu-id="bf4fc-102">Recordset.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="bf4fc-102">Recordset.Updatable Property (DAO)</span></span>


<span data-ttu-id="bf4fc-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf4fc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bf4fc-p101">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. **Boolean** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="bf4fc-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf4fc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf4fc-106">Syntax</span></span>

<span data-ttu-id="bf4fc-107">*expresión* . Actualizable</span><span class="sxs-lookup"><span data-stu-id="bf4fc-107">*expression* .Updatable</span></span>

<span data-ttu-id="bf4fc-108">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="bf4fc-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf4fc-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf4fc-109">Remarks</span></span>

<span data-ttu-id="bf4fc-110">Objetos Recordset de tipo Snapshot y forward-only siempre devuelven **False**.</span><span class="sxs-lookup"><span data-stu-id="bf4fc-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="bf4fc-p102">Muchos tipos de objetos pueden contener campos que no se pueden actualizar. Por ejemplo, puede crear un objeto **Recordset** de tipo Dynaset en el que sólo se pueden modificar algunos campos. Estos campos pueden ser fijos o contener datos que se incrementen automáticamente, o el Dynaset puede resultar de una consulta que combina tablas actualizables y no actualizables.</span><span class="sxs-lookup"><span data-stu-id="bf4fc-p102">Many types of objects can contain fields that can't be updated. For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed. These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="bf4fc-p103">Si el objeto únicamente contiene campos de sólo lectura, el valor de la propiedad **Updatable** es **False**. Si uno o más campos son actualizables, el valor de la propiedad es **True**. Sólo se pueden editar los campos actualizables. Si intenta asignar un nuevo valor a un campo de sólo lectura, se producirá un error capturable.</span><span class="sxs-lookup"><span data-stu-id="bf4fc-p103">If the object contains only read-only fields, the value of the **Updatable** property is **False**. When one or more fields are updatable, the property's value is **True**. You can edit only the updatable fields. A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="bf4fc-118">Como un objeto actualizable puede contener campos de solo lectura, compruebe la propiedad **DataUpdatable** de cada campo en la colección **Fields** de un objeto **Recordset** antes de modificar un registro.</span><span class="sxs-lookup"><span data-stu-id="bf4fc-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

