---
title: Instancia de disco y tablas de caché
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d556ff4d-e2f3-4c83-a93f-b1bfda5abc8c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 27b21162c53a64675abbf31a8ab512719b413d5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583165"
---
# <a name="disk-instances-and-cache-tables"></a>Instancia de disco y tablas de caché

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para activar un formulario, sus archivos ejecutables deben estar disponibles en el equipo del usuario. Si no están disponibles, deben copiarse desde la biblioteca de formularios en el disco local. Para ello, el Administrador de formulario predeterminado crea un subdirectorio en el directorio de Windows del usuario para que contenga los archivos del formulario ejecutable (. Exe. HLPs). Este directorio se conoce como la instancia de disco del formulario.
  
El Administrador de formulario predeterminado mantiene una tabla de todas las instancias de disco de modo que si ya existe una instancia de disco se puede utilizar sin tener que copiar los archivos de la biblioteca de formularios en el disco del usuario. En la tabla de instancias de disco se administra como una memoria caché utilizados con menos frecuencia. Si es necesaria una nueva instancia del disco, se copia en el equipo del usuario, reemplazando la instancia de disco utilizados con menos frecuencia. A continuación, se actualiza la tabla de memoria caché de disco instancia para reflejar la configuración más reciente. El tamaño de la caché de disco es una opción configurable por el usuario, permitir a los usuarios equilibrar la velocidad con la capacidad de disco disponible.
  
Además de la memoria caché la instancia de disco, el Administrador de formulario predeterminado mantiene una tabla de instancia de ejecución que se enumera todas las instancias en ejecución de los servidores de formulario en el equipo del usuario. Esto usa capacidad de MAPI para conservar instancias de formulario inactivo que se ejecuta en un estado invisible hasta que una forma de los mensajes del servidor se activa la clase de formulario. En otras palabras, se pueden almacenar en caché los servidores de formulario en la memoria RAM para minimizar el número de veces que debe ser que se encuentra dentro de una biblioteca de formularios ejecutable de un formulario y se ha cargado en la memoria desde el disco o a través de la red. Al igual que la memoria caché la instancia de disco, la memoria caché de instancia que se está ejecutando se comporta de forma menos frecuente para que una instancia de formulario que se está ejecutando se puede purgar de la memoria caché para dejar espacio para otra instancia de formulario. Esta caché se busca una instancia en ejecución de un servidor de formulario antes de que las bibliotecas de formularios se buscan en el servidor de formulario.
  
> [!NOTE]
> El Administrador de formulario predeterminado muestra un indicador de progreso al instalar un formulario en la estación de trabajo de un usuario, lo que permite al usuario cancelar la operación. Esto es especialmente útil si la conexión del usuario al archivo ejecutable del servidor de formulario es a través de una red de ancho de banda bajo. 
  
## <a name="see-also"></a>Recursos adicionales

- [Formularios MAPI](mapi-forms.md)

