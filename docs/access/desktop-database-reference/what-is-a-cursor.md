---
title: ¿Qué es un cursor?  (Referencia de escritorio de la base de datos de access)
TOCTitle: What is a Cursor?
ms:assetid: cc70d941-05e0-9b14-1c5d-6b1a5802f546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250013(v=office.15)
ms:contentKeyID: 48547738
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2023b39620f80e6f770153e381c74d5285d027c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718941"
---
# <a name="what-is-a-cursor"></a>¿Qué es un cursor?


**Se aplica a**: Access 2013, Office 2013

Las operaciones de una base de datos relacional actúan sobre un conjunto completo de filas. El conjunto de filas devuelto por una instrucción SELECT está formado por todas las filas que cumplen las condiciones de la cláusula WHERE de la instrucción. Este conjunto completo de filas devuelto por la instrucción se conoce como el conjunto de resultados. Las aplicaciones, especialmente aquéllas que son interactivas y funcionan conectadas en línea, no pueden trabajar siempre eficazmente con todo el conjunto de resultados como una unidad. Estas aplicaciones necesitan un mecanismo que trabaje cada vez con una fila o un bloque pequeño de filas. Los cursores son una extensión de los conjuntos de resultados que proporciona ese mecanismo.

Un cursor se implementa mediante una biblioteca de cursores. Una biblioteca de cursores es software, implementado a menudo como parte de un sistema de base de datos o de una API de acceso a datos, que se utiliza para administrar atributos de los datos devueltos desde un origen de datos (un conjunto de resultados). Estos atributos incluyen la administración de la concurrencia, la posición en el conjunto de resultados, el número de filas devueltas y si se puede o no avanzar y/o retroceder por el conjunto de resultados (capacidad de desplazamiento).

Un cursor realiza un seguimiento de la posición en el conjunto de resultados y permite realizar varias operaciones fila por fila en un conjunto de resultados, con o sin retorno a la tabla original. Es decir, los cursores devuelven conceptualmente un conjunto de resultados basado en las tablas de las bases de datos. El cursor se denomina así porque indica la posición actual en el conjunto de resultados, al igual que el cursor de una pantalla indica la posición actual en la misma.

Es importante familiarizarse con el concepto de cursores antes de pasar a aprender los detalles de su uso en ADO.

Mediante el uso de los cursores, puede:

  - Especificar el posicionamiento del conjunto de resultados en filas específicas.

  - Recuperar una fila o un bloque de filas según la posición actual del conjunto de resultados.

  - Modificar los datos de las filas de la posición actual del conjunto de resultados.

  - Definir diferentes niveles de sensibilidad a los cambios en los datos realizados por otros usuarios.

Por ejemplo, considere una aplicación que muestra una lista de los productos disponibles para un posible comprador. El comprador se desplaza por la lista para ver los detalles de los productos y los precios y, finalmente, selecciona un producto para su adquisición. Se producen desplazamientos y selecciones adicionales para el resto de la lista. Sin embargo, en lo que respecta al comprador, los productos aparecen de uno en uno, aunque la aplicación utilice un cursor desplazable para examinar el conjunto de resultados hacia arriba y hacia abajo.

Los cursores se pueden utilizar de varias formas:

  - Con ninguna fila.

  - Con alguna o todas las filas de una sola tabla.

  - Con alguna o todas las filas de tablas unidas lógicamente.

  - Como de sólo lectura o actualizables en el nivel de cursor o de campo.

  - Como de sólo avance o con desplazamiento completo.

  - Con el conjunto de claves de cursor ubicado en el servidor.

  - Con sensibilidad a los cambios de tablas subyacentes ocasionados por otras aplicaciones (como pertenencia a grupos de usuarios, ordenación, inserciones, actualizaciones y eliminaciones).

  - Con presencia en el servidor o en el cliente.

Los cursores de sólo lectura ayudan a los usuarios a examinar el conjunto de resultados, mientras que los cursores de lectura y escritura permiten implementar actualizaciones en filas individuales. Es posible definir cursores complejos mediante conjuntos de claves que apuntan de vuelta a filas de tablas base. Aunque algunos cursores son de sólo lectura y avance, otros se pueden mover hacia adelante y hacia atrás y proporcionar una actualización dinámica del conjunto de resultados, según los cambios realizados por otras aplicaciones en la base de datos.

No todas las aplicaciones necesitan utilizar cursores para obtener acceso a datos o para actualizarlos. Algunas consultas simplemente no requieren actualización directa de filas mediante un cursor. Los cursores deben ser una de las últimas técnicas empleadas para recuperar datos (y, en ese caso, debe elegir el cursor de menor impacto posible). Al crear un conjunto de resultados mediante un procedimiento almacenado, no es posible actualizar el conjunto de resultados mediante métodos de modificación o actualización con cursores.

## <a name="concurrency"></a>Concurrencia

En algunas aplicaciones multiusuario, es de vital importancia que los datos presentados al usuario final estén lo más actualizados que sea posible. Un ejemplo clásico es el de un sistema de reservas de una línea aérea, donde puede haber muchos usuarios que deseen el mismo asiento en un vuelo determinado (y, por tanto, un único registro). En estos casos, el diseño de la aplicación debe controlar las operaciones simultáneas en un registro.

En otras aplicaciones, la concurrencia no es tan importante. En tales casos, no se justifica el gasto de recursos para mantener los datos actualizados en todo momento.

## <a name="position"></a>Posición

Asimismo, un cursor realiza un seguimiento de la posición actual en un conjunto de resultados. Piense en la posición de un cursor como un puntero al registro actual (es similar a la forma en que un índice de una matriz apunta a su valor asociado dentro de esa matriz).

## <a name="scrollability"></a>Capacidad de desplazamiento

El tipo de cursor que usa una aplicación también afecta a la capacidad de avanzar o retroceder por las filas de un conjunto de resultados; este proceso se denomina a veces capacidad de desplazamiento. La capacidad para mover hacia delante *y* hacia atrás a través de un conjunto de resultados agrega a la complejidad del cursor y, por lo tanto, es más costosa de implementar. Por ello, sólo debe pedir un cursor con esta funcionalidad cuando sea estrictamente necesario.

