---
title: La familia de bibliotecas de ADO
TOCTitle: The ADO family of libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 296e05118054ec045c23cd92a399afdc3cddd9a1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718220"
---
# <a name="the-ado-family-of-libraries"></a>La familia de bibliotecas de ADO

**Se aplica a**: Access 2013, Office 2013

Tres bibliotecas principales componen la familia ADO: ADO (incluyendo RDS), ADO MD y ADOX.

## <a name="ado"></a>ADO

ADO permite a las aplicaciones cliente el acceso a datos de un servidor de base de datos y su manipulación a través de un proveedor OLE DB. Las principales ventajas de ADO son la facilidad de uso, la alta velocidad, el bajo nivel de consumo de memoria y la poca ocupación de espacio en disco. ADO admite las características principales para crear aplicaciones basadas en web y cliente/servidor.

ADO también incluye el servicio de datos remotos (RDS), mediante el cual puede mover datos de un servidor a una aplicación de cliente o una página Web, manipular los datos en el cliente y devolver actualizaciones al servidor en un solo viaje de ida y.

## <a name="ado-md"></a>ADO MD

Microsoft ActiveX Data Objects (MultiDimensional) (ADO MD) proporciona acceso sencillo a datos multidimensionales de lenguajes como Microsoft Visual Basic, Microsoft Visual C++ y Microsoft Visual J++. ADO MD es una ampliación de ADO que incluye objetos específicos de datos multidimensionales, como los objetos **CubeDef** y **Cellset**. Con ADO MD, puede explorar un esquema multidimensional, consultar un cubo y recuperar los resultados.

Al igual que ADO, ADO MD utiliza un proveedor OLE DB subyacente para obtener acceso a datos. Para trabajar con ADO MD, debe utilizarse un proveedor de datos multidimensionales (MDP) según se define en las especificaciones de OLE DB para OLAP. Los proveedores de datos multidimensionales presentan datos en vistas multidimensionales, al contrario que los proveedores de datos tabulares (TDP), que presentan datos en vistas tabulares. Vea la documentación correspondiente a su proveedor OLE DB para OLAP para obtener información más detallada acerca de la sintaxis y los comportamientos específicos que admite su proveedor.

## <a name="adox"></a>ADOX

Microsoft ActiveX Extensiones de ADO para lenguaje de definición de datos y seguridad (ADOX) es una extensión de los objetos y el modelo de programación de ADO. ADOX incluye objetos para creación y modificación de esquemas, así como de seguridad. Dado que se trata de un enfoque basado en objetos para la manipulación de esquemas, se puede escribir código que funcionará con diversos orígenes de datos, independientemente de las diferencias de sus sintaxis nativas.

ADOX es una biblioteca complementaria a los objetos ADO básicos. Expone objetos adicionales para crear, modificar y eliminar objetos de esquema, como tablas y procedimientos. También incluye objetos de seguridad para mantener usuarios y grupos, y para conceder y revocar permisos en objetos.

