---
title: La familia de bibliotecas ADO
TOCTitle: The ADO Family of Libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9de96854eb08ff73fe9f70edf35dee972fd1a31e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483995"
---
# <a name="the-ado-family-of-libraries"></a><span data-ttu-id="4a0a7-102">La familia de bibliotecas ADO</span><span class="sxs-lookup"><span data-stu-id="4a0a7-102">The ADO Family of Libraries</span></span>


<span data-ttu-id="4a0a7-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a0a7-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="4a0a7-104">Tres bibliotecas principales componen la familia ADO: ADO (incluyendo RDS), ADO MD y ADOX.</span><span class="sxs-lookup"><span data-stu-id="4a0a7-104">Three major libraries make up the ADO family: ADO (including RDS), ADO MD, and ADOX.</span></span>

## <a name="ado"></a><span data-ttu-id="4a0a7-105">ADO</span><span class="sxs-lookup"><span data-stu-id="4a0a7-105">ADO</span></span>

<span data-ttu-id="4a0a7-p101">ADO permite a las aplicaciones cliente el acceso a datos de un servidor de base de datos y su manipulación a través de un proveedor OLE DB. Las principales ventajas de ADO son la facilidad de uso, la alta velocidad, el bajo nivel de consumo de memoria y la poca ocupación de espacio en disco. ADO es compatible con características clave para generación de aplicaciones cliente/servidor y aplicaciones basadas en Web.</span><span class="sxs-lookup"><span data-stu-id="4a0a7-p101">ADO enables your client applications to access and manipulate data from a database server through an OLE DB provider. The primary benefits of ADO are ease of use, high speed, low memory overhead, and a small disk footprint. ADO supports key features for building client/server and Web-based applications.</span></span>

<span data-ttu-id="4a0a7-109">ADO también incluye el Servicio de datos remoto (RDS), que permite mover datos desde un servidor a una aplicación cliente o una página Web, manipular los datos en el cliente y devolver actualizaciones al servidor de una sola vez.</span><span class="sxs-lookup"><span data-stu-id="4a0a7-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or Web page, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="4a0a7-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="4a0a7-110">ADO MD</span></span>

<span data-ttu-id="4a0a7-p102">Microsoft ActiveX Data Objects (MultiDimensional) (ADO MD) proporciona acceso sencillo a datos multidimensionales de lenguajes como Microsoft Visual Basic, Microsoft Visual C++ y Microsoft Visual J++. ADO MD es una ampliación de ADO que incluye objetos específicos de datos multidimensionales, como los objetos **CubeDef** y **Cellset**. Con ADO MD, puede explorar un esquema multidimensional, consultar un cubo y recuperar los resultados.</span><span class="sxs-lookup"><span data-stu-id="4a0a7-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends ADO to include objects specific to multidimensional data, such as the **CubeDef** and **Cellset** objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="4a0a7-p103">Al igual que ADO, ADO MD utiliza un proveedor OLE DB subyacente para obtener acceso a datos. Para trabajar con ADO MD, debe utilizarse un proveedor de datos multidimensionales (MDP) según se define en las especificaciones de OLE DB para OLAP. Los proveedores de datos multidimensionales presentan datos en vistas multidimensionales, al contrario que los proveedores de datos tabulares (TDP), que presentan datos en vistas tabulares. Vea la documentación correspondiente a su proveedor OLE DB para OLAP para obtener información más detallada acerca de la sintaxis y los comportamientos específicos que admite su proveedor.</span><span class="sxs-lookup"><span data-stu-id="4a0a7-p103">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLE DB for OLAP provider for more detailed information about the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="4a0a7-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="4a0a7-118">ADOX</span></span>

<span data-ttu-id="4a0a7-p104">Microsoft ActiveX Extensiones de ADO para lenguaje de definición de datos y seguridad (ADOX) es una extensión de los objetos y el modelo de programación de ADO. ADOX incluye objetos para creación y modificación de esquemas, así como de seguridad. Dado que se trata de un enfoque basado en objetos para la manipulación de esquemas, se puede escribir código que funcionará con diversos orígenes de datos, independientemente de las diferencias de sus sintaxis nativas.</span><span class="sxs-lookup"><span data-stu-id="4a0a7-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="4a0a7-p105">ADOX es una biblioteca complementaria a los objetos ADO básicos. Expone objetos adicionales para crear, modificar y eliminar objetos de esquema, como tablas y procedimientos. También incluye objetos de seguridad para mantener usuarios y grupos, y para conceder y revocar permisos en objetos.</span><span class="sxs-lookup"><span data-stu-id="4a0a7-p105">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups, and to grant and revoke permissions on objects.</span></span>

