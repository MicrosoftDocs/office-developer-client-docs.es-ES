---
title: Programación ADO/WFC
TOCTitle: ADO/WFC programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 58ec04f92bf4d1eaaa8ea36c5937cae0bab3729f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943825"
---
# <a name="adowfc-programming"></a>Programación ADO/WFC

**Se aplica a**: Access 2013, Office 2013

En el caso de Microsoft Visual J++ 6.0, ADO se ha ampliado para trabajar con Windows Foundation Classes (WFC) de las siguientes formas. Primero, se ha implementado un conjunto de clases de Java que amplía las interfaces con ADO y crea notificaciones interesantes para los programadores de Java; las clases de Java también exponen funciones que devuelven al usuario tipos de Java. Para mejorar el rendimiento, la clase Java obtiene acceso directamente a los tipos de datos nativos del objeto de conjunto de filas OLE DB y los devuelve al programador como tipos Java sin convertirlos antes a o desde un tipo Variant. ADO se ha ampliado también para trabajar con notificaciones de eventos en el marco de trabajo de WFC.

ADO para Windows Foundation Classes (ADO/WFC) admite todos los métodos, propiedades, objetos y eventos estándar de ADO. Sin embargo, las operaciones que requieren un Variant como parámetro y que muestran un rendimiento excelente en un lenguaje como Microsoft Visual Basic muestran un menor rendimiento en un lenguaje como Visual J++. Por ello, ADO/WFC también proporciona funciones de acceso al contenido del objeto [Field](field-object-ado.md) que utilizan tipo de datos nativos de Java en lugar del tipo de datos Variant.

Para obtener información detallada dentro de la documentación ADO acerca de paquetes ADO/WFC, vea el [Índice de sintaxis ADO/WFC](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).

## <a name="referencing-the-library"></a>Hacer referencia a la biblioteca

Para importar las clases de datos ADO/WFC en un proyecto, incluya la línea siguiente en el código:

```java 
 
import com.ms.wfc.data.*; 
```

