---
title: Componentes y proveedores de servicios
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 03447b9977c74484eb7455a75fc2255c33c5e4c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717247"
---
# <a name="service-providers-and-components"></a><span data-ttu-id="77d79-102">Componentes y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="77d79-102">Service providers and components</span></span>


<span data-ttu-id="77d79-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77d79-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77d79-104">Los proveedores de servicios son componentes que amplían la funcionalidad de los proveedores de datos mediante la implementación de interfaces extendidas que el almacén de datos no admite de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="77d79-104">Service providers are components that extend the functionality of data providers by implementing extended interfaces that are not natively supported by the data store.</span></span>

<span data-ttu-id="77d79-105">Microsoft Data Access proporciona una *arquitectura de componentes* que permite que los componentes individuales y especializados implementar discretos conjuntos de funcionalidad de la base de datos, o "servicios", en almacenes con menos funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="77d79-105">Microsoft Data Access provides a *component architecture* that allows individual, specialized components to implement discrete sets of database functionality, or "services," on top of less capable stores.</span></span> <span data-ttu-id="77d79-106">En vez de obligar a que cada almacén de datos proporcione su propia implementación de la funcionalidad ampliada o forzar a las aplicaciones genéricas a que implementen internamente la funcionalidad de base de datos, los componentes de servicios proporcionan una implementación común que puede ser utilizada por cualquier aplicación al obtener acceso a cualquier almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="77d79-106">Thus, rather than forcing each data store to provide its own implementation of extended functionality or forcing generic applications to implement database functionality internally, service components provide a common implementation that any application can use when accessing any data store.</span></span> <span data-ttu-id="77d79-107">El hecho de que una parte de la funcionalidad la implemente de forma nativa el almacén de datos y la otra mediante componentes genéricos es transparente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="77d79-107">The fact that some functionality is implemented natively by the data store and some through generic components is transparent to the application.</span></span>

<span data-ttu-id="77d79-p102">Por ejemplo, un motor de cursor, como el Servicio de cursores de Microsoft para OLE DB, es un componente de servicio que puede consumir datos de un almacén de datos secuencial de sólo avance y generar datos desplazables. Otros proveedores de servicios que suele usar ADO son el Proveedor OLE DB de persistencia de Microsoft (para guardar datos en un archivo), el Servicio de forma de datos de Microsoft para OLE DB (para objetos **Recordset** jerárquicos) y el Proveedor de acceso remoto de Microsoft para OLE DB (para llamar a proveedores de datos en un equipo remoto).</span><span class="sxs-lookup"><span data-stu-id="77d79-p102">For example, a cursor engine, such as the Microsoft Cursor Service for OLE DB, is a service component that can consume data from a sequential, forward-only data store to produce scrollable data. Other service providers commonly used by ADO include the Microsoft OLE DB Persistence Provider (for saving data to a file), the Microsoft Data Shaping Service for OLE DB (for hierarchical **Recordsets**), and the Microsoft OLE DB Remoting Provider (for invoking data providers on a remote computer).</span></span>

<span data-ttu-id="77d79-110">Para obtener más información acerca de proveedores de servicios y datos, vea [Apéndice A: Proveedores](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="77d79-110">For more information about service and data providers, see [Appendix A: Providers](appendix-a-providers.md).</span></span>

