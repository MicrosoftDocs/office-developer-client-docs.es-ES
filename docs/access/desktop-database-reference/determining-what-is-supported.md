---
title: Determinación de lo que es compatible
TOCTitle: Determining what is supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3abef84f05ad279edba1fcc753f0b412a807a7b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293913"
---
# <a name="determining-what-is-supported"></a><span data-ttu-id="f8e8d-102">Determinación de lo que es compatible</span><span class="sxs-lookup"><span data-stu-id="f8e8d-102">Determining what is supported</span></span>

<span data-ttu-id="f8e8d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8e8d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8e8d-104">El método **Supports** sirve para determinar si un objeto **Recordset** especificado admite un tipo determinado de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="f8e8d-104">The **Supports** method is used to determine whether a specified **Recordset** object supports a particular type of functionality.</span></span> <span data-ttu-id="f8e8d-105">Tiene la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="f8e8d-105">It has the following syntax:</span></span>

`boolean = recordset.Supports( CursorOptions )`

<span data-ttu-id="f8e8d-p102">**Supports** devuelve un valor booleano que indica si el proveedor admite todas las características identificadas mediante el argumento *CursorOptions*. Puede usar el método **Supports** para determinar qué tipos de funcionalidades admite un objeto **Recordset**. Si el objeto **Recordset** admite las características cuyas constantes correspondientes están en *CursorOptions*, el método **Supports** devuelve **True**. De lo contrario, devuelve **False**.</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p102">**Supports** returns a Boolean value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider. You can use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>

<span data-ttu-id="f8e8d-p103">Con el método **Supports**, puede comprobar la disponibilidad del objeto **Recordset** para agregar nuevos registros, usar marcadores, usar el método **Find**, usar el desplazamiento, usar la propiedad **Index** y realizar actualizaciones por lotes. Para consultar una lista completa de constantes y sus significados, vea [CursorOptionEnum](cursoroptionenum.md).</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p103">Using the **Supports** method, you can check for the ability of the **Recordset** object to add new records, use bookmarks, use the **Find** method, use scrolling, use the **Index** property, and to perform batch updates. For a complete list of constants and their meanings, see [CursorOptionEnum](cursoroptionenum.md).</span></span>

<span data-ttu-id="f8e8d-p104">Aunque el método **Supports** puede devolver **True** para una funcionalidad determinada, no garantiza que el proveedor pueda ofrecer la funcionalidad en cualquier circunstancia. El método **Supports** simplemente indica si el proveedor puede admitir la funcionalidad especificada, suponiendo que se cumplen ciertas condiciones. Por ejemplo, el método **Supports** puede indicar que un objeto **Recordset** admite actualizaciones, incluso aunque el cursor se base en una unión de varias tablas (con algunas columnas que no se pueden actualizar).</span><span class="sxs-lookup"><span data-stu-id="f8e8d-p104">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the **Supports** method may indicate that a **Recordset** object supports updates, even though the cursor is based on a multiple table join — some columns of which are not updateable.</span></span>

