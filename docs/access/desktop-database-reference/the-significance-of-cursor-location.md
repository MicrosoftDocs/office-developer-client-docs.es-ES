---
title: La importancia de la ubicación del cursor
TOCTitle: The Significance of Cursor Location
ms:assetid: 57cf91a0-2612-b1ca-1c03-9c1ccb396b2e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249296(v=office.15)
ms:contentKeyID: 48544978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e1b552ac2774fe0c5d47c19924219800e5bdf865
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484195"
---
# <a name="the-significance-of-cursor-location"></a>La importancia de la ubicación del cursor


**Se aplica a**: Access 2013 | Office 2013

Cada cursor utiliza recursos temporales para almacenar sus datos. Estos recursos pueden ser memoria, un archivo de paginación de disco, archivos temporales en el disco o incluso almacenamiento temporal en la base de datos. El cursor se denomina un cursor *de cliente* cuando estos recursos están ubicados en el equipo cliente. El cursor se denomina cursor de *servidor* cuando estos recursos están ubicados en el servidor.

## <a name="client-side-cursors"></a>Cursores de cliente

En ADO, para llamar a un cursor de cliente se utiliza el valor **adUseClient** de **CursorLocationEnum**. Con un cursor de cliente sin conjunto de claves, el servidor envía todo el conjunto de resultados al equipo cliente a través de la red. El equipo cliente proporciona y administra los recursos temporales que necesita el cursor y el conjunto de resultados. La aplicación del cliente puede examinar el conjunto completo de resultados para determinar qué filas requiere.

Los cursores de cliente estáticos y los controlados por conjuntos de claves pueden cargar de manera importante su estación de trabajo si incluyen demasiadas filas. Aunque todas las bibliotecas de cursores tienen capacidad para crear cursores con miles de filas, las aplicaciones diseñadas para recuperar conjuntos de filas tan grandes pueden tener un bajo rendimiento. Por supuesto, hay excepciones. Para algunas aplicaciones, un cursor de cliente grande podría ser perfectamente apropiado sin que el rendimiento fuese un problema.

Una ventaja obvia del cursor de cliente es la rapidez de la respuesta. Una vez descargado el conjunto de resultados en el equipo cliente, se pueden examinar las filas muy rápido. Por lo general, la aplicación es más escalable con cursores de cliente porque los requisitos de recursos del cursor se aplican en cada cliente por separado y no en el servidor.

## <a name="server-side-cursors"></a>Cursores de servidor

En ADO, para llamar para un cursor de servidor se utiliza el valor **adUseServer** de **CursorLocationEnum**. Con un cursor de servidor, el servidor administra el conjunto de resultados utilizando recursos proporcionados por el equipo servidor. El cursor de servidor devuelve sólo los datos solicitados a través de la red. Este tipo de cursor puede proporcionar a veces mejor rendimiento que el cursor de cliente, especialmente en situaciones en las que un tráfico excesivo en la red es un problema.

No obstante, es importante señalar que un cursor de servidor consume (temporalmente al menos) valiosos recursos del servidor para cada cliente activo. Debe planear en consecuencia para asegurarse de que el hardware del servidor tenga capacidad para administrar todos los cursores de servidor solicitados por clientes activos. Además, un cursor de servidor puede ser lento porque sólo proporciona acceso a una fila (no hay lotes de cursores disponibles).

Los cursores de servidor son útiles para insertar, actualizar o eliminar registros. Con cursores de servidor, se pueden tener varias instrucciones activas en la misma conexión.

