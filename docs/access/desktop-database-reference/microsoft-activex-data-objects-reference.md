---
title: Referencia de objetos de datos ActiveX de Microsoft
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c1fee657c0d6ecd319157f704df2b1c5a900be3b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698886"
---
# <a name="microsoft-activex-data-objects-reference"></a><span data-ttu-id="cff15-102">Referencia de objetos de datos ActiveX de Microsoft</span><span class="sxs-lookup"><span data-stu-id="cff15-102">Microsoft ActiveX Data Objects reference</span></span>

<span data-ttu-id="cff15-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cff15-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="purpose"></a><span data-ttu-id="cff15-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="cff15-104">Purpose</span></span>

<span data-ttu-id="cff15-105">Microsoft ActiveX Data Objects (ADO) permite a las aplicaciones cliente el acceso a datos de un servidor de base de datos y su manipulación a través de un proveedor OLE DB.</span><span class="sxs-lookup"><span data-stu-id="cff15-105">Microsoft ActiveX Data Objects (ADO) enable your client applications to access and manipulate data from a database server through an OLE DB provider.</span></span> <span data-ttu-id="cff15-106">Sus principales ventajas son la facilidad de uso, la alta velocidad, el bajo nivel de consumo de memoria y la poca ocupación de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="cff15-106">Its primary benefits are ease of use, high speed, low memory overhead, and a small disk footprint.</span></span> <span data-ttu-id="cff15-107">ADO admite las características principales para crear aplicaciones basadas en web y cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="cff15-107">ADO supports key features for building client/server and web-based applications.</span></span>

## <a name="rds"></a><span data-ttu-id="cff15-108">RDS</span><span class="sxs-lookup"><span data-stu-id="cff15-108">RDS</span></span>

<span data-ttu-id="cff15-109">ADO también incluye el servicio de datos remotos (RDS), mediante el cual puede mover datos de un servidor a una aplicación de cliente o una página Web, manipular los datos en el cliente y devolver actualizaciones al servidor en un solo viaje de ida y.</span><span class="sxs-lookup"><span data-stu-id="cff15-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or webpage, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="cff15-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="cff15-110">ADO MD</span></span>

<span data-ttu-id="cff15-p102">Microsoft ActiveX Data Objects (MultiDimensional) (ADO MD) proporciona acceso sencillo a datos multidimensionales de lenguajes como Microsoft Visual Basic, Microsoft Visual C++ y Microsoft Visual J++. ADO MD es una ampliación de Microsoft ActiveX Data Objects (ADO) que incluye objetos específicos de datos multidimensionales, como los objetos CubeDef y Cellset. Con ADO MD, puede explorar un esquema multidimensional, consultar un cubo y recuperar los resultados.</span><span class="sxs-lookup"><span data-stu-id="cff15-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the CubeDef and Cellset objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="cff15-p103">Al igual que ADO, ADO MD utiliza un proveedor OLE DB subyacente para obtener acceso a datos. Para trabajar con ADO MD, debe utilizarse un proveedor de datos multidimensionales (MDP) según se define en las especificaciones de OLE DB para OLAP. Los proveedores de datos multidimensionales presentan datos en vistas multidimensionales, al contrario que los proveedores de datos tabulares (TDP), que presentan datos en vistas tabulares. Vea la documentación correspondiente a su proveedor OLE DB para OLAP para obtener información más detallada acerca de la sintaxis y los comportamientos específicos que admite su proveedor.</span><span class="sxs-lookup"><span data-stu-id="cff15-p103">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="cff15-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="cff15-118">ADOX</span></span>

<span data-ttu-id="cff15-p104">Microsoft ActiveX Extensiones de ADO para lenguaje de definición de datos y seguridad (ADOX) es una extensión de los objetos y el modelo de programación de ADO. ADOX incluye objetos para creación y modificación de esquemas, así como de seguridad. Dado que se trata de un enfoque basado en objetos para la manipulación de esquemas, se puede escribir código que funcionará con diversos orígenes de datos, independientemente de las diferencias de sus sintaxis nativas.</span><span class="sxs-lookup"><span data-stu-id="cff15-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="cff15-p105">ADOX es una biblioteca complementaria a los objetos ADO básicos. Expone objetos adicionales para crear, modificar y eliminar objetos de esquema, como tablas y procedimientos. También incluye objetos de seguridad para mantener usuarios y grupos, y para conceder y revocar permisos en objetos.</span><span class="sxs-lookup"><span data-stu-id="cff15-p105">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

## <a name="ado-25-main-components"></a><span data-ttu-id="cff15-125">ADO 2.5 componentes principales</span><span class="sxs-lookup"><span data-stu-id="cff15-125">ADO 2.5 main components</span></span>

- <span data-ttu-id="cff15-126">[Guía del programador](ado-programmer-s-guide.md): Introducción al uso de ADO, RDS, ADO MD y ADOX.</span><span class="sxs-lookup"><span data-stu-id="cff15-126">[Programmer's guide](ado-programmer-s-guide.md): An introduction to using ADO, RDS, ADO MD, and ADOX.</span></span>

- <span data-ttu-id="cff15-127">[Referencia del programador](ado-programmer-s-reference-topics.md): en esta sección de la documentación de ADO contiene temas para cada colección ADO, RDS, ADO MD y objetos ADOX, (propiedad), propiedad dinámica, método, evento y (enumeración).</span><span class="sxs-lookup"><span data-stu-id="cff15-127">[Programmer's reference](ado-programmer-s-reference-topics.md): This section of the ADO documentation contains topics for each ADO, RDS, ADO MD, and ADOX object, collection, property, dynamic property, method, event, and enumeration.</span></span>

## <a name="feedback"></a><span data-ttu-id="cff15-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cff15-128">Feedback</span></span>

<span data-ttu-id="cff15-129">Puede enviar comentarios acerca de la documentación o los ejemplos de ADO directamente al equipo de documentación de ADO.</span><span class="sxs-lookup"><span data-stu-id="cff15-129">You can send feedback about ADO documentation or samples directly to the ADO documentation team.</span></span>

