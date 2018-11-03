---
title: TableDefs.Refresh (método) (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53a632999f1b60b078e9365c9f99e52ddec284e9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927882"
---
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="3b487-102">TableDefs.Refresh (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="3b487-102">TableDefs.Refresh method (DAO)</span></span>


<span data-ttu-id="3b487-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b487-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b487-104">Actualiza los objetos en la colección especificada para que reflejen el esquema actual de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3b487-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b487-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b487-105">Syntax</span></span>

<span data-ttu-id="3b487-106">*expresión* . Actualización</span><span class="sxs-lookup"><span data-stu-id="3b487-106">*expression* .Refresh</span></span>

<span data-ttu-id="3b487-107">*expresión* Variable que representa un objeto **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="3b487-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b487-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b487-108">Remarks</span></span>

<span data-ttu-id="3b487-p101">Para determinar la posición que usa el motor de base de datos de Microsoft Access para objetos **Field** en la colección **Fields** de un objeto **QueryDef**, **Recordset** o **TableDef**, use la propiedad **OrdinalPosition** de cada objeto **Field**. Es posible que cambiando la propiedad **OrdinalPosition** de un objeto **Field** no se cambie el orden de los objetos **Field** de la colección hasta que se use el método **Refresh**.</span><span class="sxs-lookup"><span data-stu-id="3b487-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="3b487-p102">El método **Refresh** se utiliza en entornos multiusuario en los que otros usuarios pueden cambiar la base de datos. Es posible que se deba utilizar también en cualquier colección que se vea afectada indirectamente por los cambios en la base de datos. Por ejemplo, si cambia una colección **Users**, es posible que necesite actualizar una colección **Groups** antes de utilizar esta colección **Groups**.</span><span class="sxs-lookup"><span data-stu-id="3b487-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="3b487-p103">Una colección se rellena con objetos la primera vez que se hace referencia a ella y no reflejará automáticamente los cambios siguientes que realicen otros usuarios. Si es probable que otro usuario modifique una colección, utilice el método Refresh en la colección justo antes de ejecutar cualquier otra tarea en la aplicación que suponga la presencia o ausencia de un objeto en particular de la colección. Esto asegura que la colección esté lo más actualizada posible. Por otra parte, el uso de Refresh puede ralentizar innecesariamente el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="3b487-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

