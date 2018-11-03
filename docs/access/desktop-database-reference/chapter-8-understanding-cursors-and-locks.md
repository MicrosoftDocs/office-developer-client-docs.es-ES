---
title: 'Capítulo 8: Cursores y bloqueos'
TOCTitle: 'Chapter 8: Understanding cursors and locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ca76b5635e057251aff845ecf45146e6e0d89a6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936944"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="63e38-102">Capítulo 8: Cursores y bloqueos</span><span class="sxs-lookup"><span data-stu-id="63e38-102">Chapter 8: Understanding cursors and locks</span></span>

<span data-ttu-id="63e38-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63e38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63e38-p101">Es importante comprender cómo funcionan los cursores, para poder seleccionar el tipo de cursor mejor y más eficaz para los requisitos de acceso a datos de una aplicación. Una configuración de cursor que no sea la óptima puede provocar que las operaciones de acceso a datos sean extremadamente lentas.</span><span class="sxs-lookup"><span data-stu-id="63e38-p101">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements. A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="63e38-106">Numerosas funcionalidades del objeto **Recordset** de ADO están determinadas por el tipo y la ubicación del cursor, así como el tipo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="63e38-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="63e38-107">En este capítulo, se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="63e38-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="63e38-108">¿Qué es un cursor?</span><span class="sxs-lookup"><span data-stu-id="63e38-108">What is a cursor?</span></span>](what-is-a-cursor.md)
- [<span data-ttu-id="63e38-109">La importancia de la ubicación del cursor</span><span class="sxs-lookup"><span data-stu-id="63e38-109">The significance of cursor location</span></span>](the-significance-of-cursor-location.md)
- [<span data-ttu-id="63e38-110">El servicio de cursores de Microsoft para OLE DB</span><span class="sxs-lookup"><span data-stu-id="63e38-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)
- [<span data-ttu-id="63e38-111">Utilizar CacheSize</span><span class="sxs-lookup"><span data-stu-id="63e38-111">Using CacheSize</span></span>](using-cachesize.md)
- [<span data-ttu-id="63e38-112">Características de cursores y bloqueos</span><span class="sxs-lookup"><span data-stu-id="63e38-112">Cursor and lock characteristics</span></span>](cursor-and-lock-characteristics.md)
- [<span data-ttu-id="63e38-113">Tipos de cursores (ADO)</span><span class="sxs-lookup"><span data-stu-id="63e38-113">Types of cursors (ADO)</span></span>](types-of-cursors.md)
- [<span data-ttu-id="63e38-114">¿Qué es un bloqueo? (ADO)</span><span class="sxs-lookup"><span data-stu-id="63e38-114">What is a lock? (ADO)</span></span>](what-is-a-lock.md)

