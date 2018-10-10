---
title: Programación ADO/WFC
TOCTitle: ADO/WFC Programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88343d14a9419cbc3425e0c21dee08d243f2e697
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483842"
---
# <a name="adowfc-programming"></a><span data-ttu-id="197b7-102">Programación ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="197b7-102">ADO/WFC Programming</span></span>


<span data-ttu-id="197b7-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="197b7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="197b7-p101">En el caso de Microsoft Visual J++ 6.0, ADO se ha ampliado para trabajar con Windows Foundation Classes (WFC) de las siguientes formas. Primero, se ha implementado un conjunto de clases de Java que amplía las interfaces con ADO y crea notificaciones interesantes para los programadores de Java; las clases de Java también exponen funciones que devuelven al usuario tipos de Java. Para mejorar el rendimiento, la clase Java obtiene acceso directamente a los tipos de datos nativos del objeto de conjunto de filas OLE DB y los devuelve al programador como tipos Java sin convertirlos antes a o desde un tipo Variant. ADO se ha ampliado también para trabajar con notificaciones de eventos en el marco de trabajo de WFC.</span><span class="sxs-lookup"><span data-stu-id="197b7-p101">For Microsoft Visual J++ 6.0, ADO has been extended to work with Windows Foundation Classes (WFC) in the following ways. First, a set of Java classes has been implemented that extends the ADO interfaces and creates notifications interesting to the Java programmer; the Java classes also expose functions that return Java types to the user. To improve performance, the Java class directly accesses the native data types in the OLE DB rowset object, and returns them to the Java programmer as Java types without first converting them to and from a variant. ADO has also been extended to work with event notifications in the WFC framework.</span></span>

<span data-ttu-id="197b7-p102">ADO para Windows Foundation Classes (ADO/WFC) admite todos los métodos, propiedades, objetos y eventos estándar de ADO. Sin embargo, las operaciones que requieren un Variant como parámetro y que muestran un rendimiento excelente en un lenguaje como Microsoft Visual Basic muestran un menor rendimiento en un lenguaje como Visual J++. Por ello, ADO/WFC también proporciona funciones de acceso al contenido del objeto [Field](field-object-ado.md) que utilizan tipo de datos nativos de Java en lugar del tipo de datos Variant.</span><span class="sxs-lookup"><span data-stu-id="197b7-p102">ADO for Windows Foundation Classes (ADO/WFC) supports all the standard ADO methods, properties, objects, and events. However, operations that require a variant as a parameter and show excellent performance in a language such as Microsoft Visual Basic, display lesser performance in a language such as Visual J++. For that reason, ADO/WFC also provides accessor functions on the [Field](field-object-ado.md) object that take native Java data types instead of the variant data type.</span></span>

<span data-ttu-id="197b7-111">Para obtener información detallada dentro de la documentación ADO acerca de paquetes ADO/WFC, vea el [Índice de sintaxis ADO/WFC](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="197b7-111">For more detailed information within the ADO documentation about ADO/WFC packages, see [the ADO/WFC Syntax Index](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).</span></span>

## <a name="referencing-the-library"></a><span data-ttu-id="197b7-112">Cómo hacer referencia a la biblioteca</span><span class="sxs-lookup"><span data-stu-id="197b7-112">Referencing the Library</span></span>

<span data-ttu-id="197b7-113">Para importar las clases de datos ADO/WFC en un proyecto, incluya la línea siguiente en el código:</span><span class="sxs-lookup"><span data-stu-id="197b7-113">To import the ADO/WFC data classes into your project, include the following line in your code:</span></span>

```java 
 
import com.ms.wfc.data.*; 
```
