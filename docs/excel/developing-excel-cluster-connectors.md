---
title: Desarrollo de conectores de clúster de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412600"
---
# <a name="developing-excel-cluster-connectors"></a>Desarrollo de conectores de clúster de Excel

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Los conectores de clúster de Excel proporcionan un medio para descargar automáticamente llamadas de función definidas por el usuario seguras para clústeres en un XLL a un servidor en clúster. Para obtener una descripción de las funciones definidas por el usuario seguras para clústeres, vea [Funciones seguras de clúster.](cluster-safe-functions.md) Esta descarga puede mejorar el rendimiento al permitir el uso de más recursos informáticos. Un conector de clúster suele ser desarrollado por un proveedor de clúster de cálculo de alto rendimiento.
  
## <a name="cluster-connectors"></a>Conectores de clúster

Un conector de clúster es una DLL que proporciona puntos de entrada definidos que Excel usa para coordinar llamadas de función definidas por el usuario seguras para clústeres. Sirve como interfaz entre Excel y el clúster de cálculo de alto rendimiento, para la administración de sesiones, para realizar llamadas de función (pasando el nombre de la función completa y los argumentos reales de la llamada) y para devolver los resultados de la llamada a Excel a través de un mecanismo de devolución de llamada.
  
Para crear un conector de clúster, cree una DLL que exponga los puntos de entrada enumerados en [Funciones de conector de](excel-cluster-connector-functions.md)clúster de Excel .
  
## <a name="installing-a-cluster-connector"></a>Instalación de un conector de clúster

Para que un conector de clúster esté disponible en Excel, el código de instalación del conector debe instalar la DLL del conector en el equipo donde está instalado Excel. Además, el código de configuración del conector debe agregar una entrada para el conector en la siguiente clave del Registro:
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\
  
Agregue un nodo a esta clave para el conector de clúster que especifica las siguientes cadenas:
  
-  `Name`Nombre que aparecerá en la lista de conectores de clúster en Excel.
    
-  `Filename`La ruta de acceso completa de la DLL.
    

