---
title: Parameters.Refresh Method (DAO)
TOCTitle: Refresh Method
ms:assetid: 47db1602-e223-985d-881c-b73e2d26acb7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193228(v=office.15)
ms:contentKeyID: 48544607
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 019f59aa8663c60b349c0e39cdb27fc685a3fad0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486473"
---
# <a name="parametersrefresh-method-dao"></a><span data-ttu-id="2ff81-102">Parameters.Refresh Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="2ff81-102">Parameters.Refresh Method (DAO)</span></span>


<span data-ttu-id="2ff81-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ff81-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2ff81-104">Actualiza los objetos en la colección especificada para que reflejen el esquema actual de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="2ff81-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff81-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ff81-105">Syntax</span></span>

<span data-ttu-id="2ff81-106">*expresión* . Actualización</span><span class="sxs-lookup"><span data-stu-id="2ff81-106">*expression* .Refresh</span></span>

<span data-ttu-id="2ff81-107">*expresión* Variable que representa un objeto **Parameters** .</span><span class="sxs-lookup"><span data-stu-id="2ff81-107">*expression* A variable that represents a **Parameters** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ff81-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ff81-108">Remarks</span></span>

<span data-ttu-id="2ff81-p101">El método **Refresh** se utiliza en entornos multiusuario en los que otros usuarios pueden cambiar la base de datos. Es posible que se deba utilizar también en cualquier colección que se vea afectada indirectamente por los cambios en la base de datos. Por ejemplo, si cambia una colección **Users**, es posible que necesite actualizar una colección **Groups** antes de utilizar esta colección **Groups**.</span><span class="sxs-lookup"><span data-stu-id="2ff81-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="2ff81-p102">Una colección se rellena con objetos la primera vez que se hace referencia a ella y no reflejará automáticamente los cambios siguientes que realicen otros usuarios. Si es probable que otro usuario modifique una colección, utilice el método Refresh en la colección justo antes de ejecutar cualquier otra tarea en la aplicación que suponga la presencia o ausencia de un objeto en particular de la colección. Esto asegura que la colección esté lo más actualizada posible. Por otra parte, el uso de Refresh puede ralentizar innecesariamente el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2ff81-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

