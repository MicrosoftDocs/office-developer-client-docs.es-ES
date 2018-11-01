---
title: Relations.Refresh Method (DAO)
TOCTitle: Refresh Method
ms:assetid: d71cecf2-da90-5f62-9e51-f994e660ad34
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835058(v=office.15)
ms:contentKeyID: 48547997
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fea6525d56552129ddc697cd56adf1eb6409345
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891040"
---
# <a name="relationsrefresh-method-dao"></a><span data-ttu-id="082fb-102">Relations.Refresh Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="082fb-102">Relations.Refresh Method (DAO)</span></span>


<span data-ttu-id="082fb-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="082fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="082fb-104">Actualiza los objetos en la colección especificada para que reflejen el esquema actual de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="082fb-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="082fb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="082fb-105">Syntax</span></span>

<span data-ttu-id="082fb-106">*expresión* . Actualización</span><span class="sxs-lookup"><span data-stu-id="082fb-106">*expression* .Refresh</span></span>

<span data-ttu-id="082fb-107">*expresión* Variable que representa un objeto **Relations** .</span><span class="sxs-lookup"><span data-stu-id="082fb-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="082fb-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="082fb-108">Remarks</span></span>

<span data-ttu-id="082fb-p101">El método **Refresh** se utiliza en entornos multiusuario en los que otros usuarios pueden cambiar la base de datos. Es posible que se deba utilizar también en cualquier colección que se vea afectada indirectamente por los cambios en la base de datos. Por ejemplo, si cambia una colección **Users**, es posible que necesite actualizar una colección **Groups** antes de utilizar esta colección **Groups**.</span><span class="sxs-lookup"><span data-stu-id="082fb-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="082fb-p102">Una colección se rellena con objetos la primera vez que se hace referencia a ella y no reflejará automáticamente los cambios siguientes que realicen otros usuarios. Si es probable que otro usuario modifique una colección, utilice el método Refresh en la colección justo antes de ejecutar cualquier otra tarea en la aplicación que suponga la presencia o ausencia de un objeto en particular de la colección. Esto asegura que la colección esté lo más actualizada posible. Por otra parte, el uso de Refresh puede ralentizar innecesariamente el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="082fb-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

