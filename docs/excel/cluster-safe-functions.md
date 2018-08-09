---
title: Funciones seguras de clúster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f73f49e4d76a8545399eede283b70551ee6569f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815514"
---
# <a name="cluster-safe-functions"></a>Funciones seguras de clúster

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
En Excel 2013, Excel puede descargar las llamadas de función definida por el usuario (UDF) a un clúster de sistemas de alto rendimiento a través de una interfaz de conector de clúster dedicado. Compute Cluster Server proveedores disponen de conectores de clúster. Los autores UDF pueden declarar sus UDF como clúster seguros y, a continuación, cuando un conector de clúster está presente, Excel envía las llamadas a estos archivos de UDF para el conector de clúster para descarga.
  
Cuando Excel descubre una UDF seguras de clúster durante la actualización, se pasa el nombre del XLL que se está ejecutando actualmente, el nombre de la UDF seguras de clúster y los parámetros para el conector de clúster. El conector ejecuta la llamada UDF de forma remota y devuelve los resultados a Excel. No dependientes cálculo continúa y cuando el conector de clúster ha terminado de ejecutarse la UDF, se pasan los resultados a Excel y continuar cálculos dependientes. El mecanismo para este comportamiento asincrónico imite el mecanismo de UDF asincrónicas, excepto en que el conector de clúster administra los aspectos asincrónicos en lugar del autor UDF. Normalmente, un conector de clúster implementa una corrección de XLL para cargar los XLL y ejecutar las UDF en compute nodos de clúster.
  
La mecánica de la declaración de las UDF como seguras de clúster son similares a las de la declaración de las UDF como seguros para la actualización de cálculos multiproceso. Sin embargo, debido a que no se está ejecutando necesariamente las UDF en el mismo equipo que otros las UDF desde la misma sesión de Excel, existen diferentes consideraciones al escribir las UDF seguras de clúster.
  
Para registrar una UDF como seguras de clúster, debe llamar a la función de devolución de llamada [xlfRegister (formulario 1)](xlfregister-form-1.md) a través de la interfaz **Excel12** o **Excel12v** . Para obtener más información acerca de estas interfaces, vea la [Excel4/Excel12](excel4-excel12.md) y la [Excel4v/Excel12v](excel4v-excel12v.md). Registrar una UDF como seguras de clúster a través de la interfaz de **Excel4** o **Excel4v** no es compatible. 
  
Si se registra una función como seguras de clúster, debe asegurarse de que la función se comporta de forma segura para el clúster. Aunque el comportamiento exacto del conector de clúster es específico de la implementación, debe diseñar su UDF para ejecutar en un sistema distribuido y tienen las siguientes características:
  
- Un archivo UDF no debe confiar en cualquier estado de la memoria. Por ejemplo, un archivo UDF no debe confiar en una caché en memoria existente.
    
- Un archivo UDF no debe llevar a cabo las devoluciones de llamada de Excel que no es compatible con el proveedor de conector de clúster.
    
Además de comportamiento de seguridad de clúster, existen las siguientes restricciones técnicas de las UDF seguras de clúster:
  
1. Sin argumentos XLOPER (tipos de 'P', 'R').
    
2. Sin argumentos XLOPER12 que admiten referencias de rango (tipo 'U').
    
3. No puede ser una función equivalente de hoja macro ('#' y '&amp;' no se puede combinar).
    
Para las UDF con tiempos de ejecución, la sobrecarga de descarga puede ser mayor que el tiempo que tarda la UDF en ejecución, al negar muchas de las ventajas de usar esta infraestructura.
  
> [!NOTE]
> No se puede declarar una UDF seguras de clúster como un UDF asincrónico. 
  
Un archivo UDF puede determinar si se está ejecutando con un conector de clúster mediante una llamada a la función de devolución de llamada de [xlRunningOnCluster](xlrunningoncluster.md) . 
  

