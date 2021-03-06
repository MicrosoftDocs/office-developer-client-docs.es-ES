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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289122"
---
# <a name="microsoft-activex-data-objects-reference"></a>Referencia de objetos de datos ActiveX de Microsoft

**Se aplica a:** Access 2013, Office 2013

## <a name="purpose"></a>Objetivo

Microsoft ActiveX Data Objects (ADO) permite a las aplicaciones cliente el acceso a datos de un servidor de base de datos y su manipulación a través de un proveedor OLE DB. Sus principales ventajas son la facilidad de uso, la alta velocidad, el bajo nivel de consumo de memoria y la poca ocupación de espacio en disco. ADO es compatible con características clave para la generación de aplicaciones de cliente o servidor y aplicaciones basadas en web.

## <a name="rds"></a>RDS

ADO también incluye el Servicio de datos remoto (RDS), que permite mover datos desde un servidor a una aplicación cliente o una página web, manipular los datos en el cliente y devolver actualizaciones al servidor de una sola vez.

## <a name="ado-md"></a>ADO MD

Microsoft ActiveX Data Objects (MultiDimensional) (ADO MD) proporciona acceso sencillo a datos multidimensionales de lenguajes como Microsoft Visual Basic, Microsoft Visual C++ y Microsoft Visual J++. ADO MD es una ampliación de Microsoft ActiveX Data Objects (ADO) que incluye objetos específicos de datos multidimensionales, como los objetos CubeDef y Cellset. Con ADO MD, puede explorar un esquema multidimensional, consultar un cubo y recuperar los resultados.

Al igual que ADO, ADO MD utiliza un proveedor OLE DB subyacente para obtener acceso a datos. Para trabajar con ADO MD, debe utilizarse un proveedor de datos multidimensionales (MDP) según se define en las especificaciones de OLE DB para OLAP. Los proveedores de datos multidimensionales presentan datos en vistas multidimensionales, al contrario que los proveedores de datos tabulares (TDP), que presentan datos en vistas tabulares. Vea la documentación correspondiente a su proveedor OLE DB para OLAP para obtener información más detallada acerca de la sintaxis y los comportamientos específicos que admite su proveedor.

## <a name="adox"></a>ADOX

Microsoft ActiveX Extensiones de ADO para lenguaje de definición de datos y seguridad (ADOX) es una extensión de los objetos y el modelo de programación de ADO. ADOX incluye objetos para creación y modificación de esquemas, así como de seguridad. Dado que se trata de un enfoque basado en objetos para la manipulación de esquemas, se puede escribir código que funcionará con diversos orígenes de datos, independientemente de las diferencias de sus sintaxis nativas.

ADOX es una biblioteca complementaria a los objetos ADO básicos. Expone objetos adicionales para crear, modificar y eliminar objetos de esquema, como tablas y procedimientos. También incluye objetos de seguridad para mantener usuarios y grupos, y para conceder y revocar permisos en objetos.

## <a name="ado-25-main-components"></a>Componentes principales de ADO 2.5

- [Guía del programador](ado-programmer-s-guide.md): Introducción al uso de ADO, RDS, ADO MD y ADOX.

- [Referencia del programador](ado-programmer-s-reference-topics.md): esta sección de la documentación de ADO contiene temas para cada objeto, colección, propiedad, propiedad dinámica, método, evento y enumeración de ADO, RDS, ADO MD y ADOX.

## <a name="feedback"></a>Comentarios

Puede enviar comentarios acerca de la documentación o los ejemplos de ADO directamente al equipo de documentación de ADO.

