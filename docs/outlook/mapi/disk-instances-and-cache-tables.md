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
ms.openlocfilehash: c3b371a226c9eb6a3cf675ee316bf22a597fe806
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816680"
---
# <a name="disk-instances-and-cache-tables"></a><span data-ttu-id="33f58-103">Instancia de disco y tablas de caché</span><span class="sxs-lookup"><span data-stu-id="33f58-103">Disk Instances and Cache Tables</span></span>

<span data-ttu-id="33f58-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33f58-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="33f58-105">Para activar un formulario, sus archivos ejecutables deben estar disponibles en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="33f58-105">To activate a form, its executable files must be available on the user's computer.</span></span> <span data-ttu-id="33f58-106">Si no están disponibles, deben copiarse desde la biblioteca de formularios en el disco local.</span><span class="sxs-lookup"><span data-stu-id="33f58-106">If they are not available, they must be copied from the form library to the local disk.</span></span> <span data-ttu-id="33f58-107">Para ello, el Administrador de formulario predeterminado crea un subdirectorio en el directorio de Windows del usuario para que contenga los archivos del formulario ejecutable (. Exe. HLPs).</span><span class="sxs-lookup"><span data-stu-id="33f58-107">To do this, the default form manager creates a subdirectory in the user's Windows directory to contain the form's executable files (.EXEs,.HLPs).</span></span> <span data-ttu-id="33f58-108">Este directorio se conoce como la instancia de disco del formulario.</span><span class="sxs-lookup"><span data-stu-id="33f58-108">This directory is referred to as the disk instance of the form.</span></span>
  
<span data-ttu-id="33f58-109">El Administrador de formulario predeterminado mantiene una tabla de todas las instancias de disco de modo que si ya existe una instancia de disco se puede utilizar sin tener que copiar los archivos de la biblioteca de formularios en el disco del usuario.</span><span class="sxs-lookup"><span data-stu-id="33f58-109">The default form manager maintains a table of all disk instances so that if a disk instance already exists it can be used without having to copy files from the form library to the user's disk.</span></span> <span data-ttu-id="33f58-110">En la tabla de instancias de disco se administra como una memoria caché utilizados con menos frecuencia.</span><span class="sxs-lookup"><span data-stu-id="33f58-110">The table of disk instances is managed as a least-frequently-used cache.</span></span> <span data-ttu-id="33f58-111">Si es necesaria una nueva instancia del disco, se copia en el equipo del usuario, reemplazando la instancia de disco utilizados con menos frecuencia.</span><span class="sxs-lookup"><span data-stu-id="33f58-111">If a new disk instance is needed, it is copied to the user's computer, replacing the least-frequently-used disk instance.</span></span> <span data-ttu-id="33f58-112">A continuación, se actualiza la tabla de memoria caché de disco instancia para reflejar la configuración más reciente.</span><span class="sxs-lookup"><span data-stu-id="33f58-112">The disk instance cache table is then updated to reflect the latest configuration.</span></span> <span data-ttu-id="33f58-113">El tamaño de la caché de disco es una opción configurable por el usuario, permitir a los usuarios equilibrar la velocidad con la capacidad de disco disponible.</span><span class="sxs-lookup"><span data-stu-id="33f58-113">The size of the disk cache is a user-configurable option, enabling users to balance speed with available disk capacity.</span></span>
  
<span data-ttu-id="33f58-114">Además de la memoria caché la instancia de disco, el Administrador de formulario predeterminado mantiene una tabla de instancia de ejecución que se enumera todas las instancias en ejecución de los servidores de formulario en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="33f58-114">In addition to the disk instance cache, the default form manager maintains a running instance table that lists all running instances of form servers on the user's computer.</span></span> <span data-ttu-id="33f58-115">Esto usa capacidad de MAPI para conservar instancias de formulario inactivo que se ejecuta en un estado invisible hasta que una forma de los mensajes del servidor se activa la clase de formulario.</span><span class="sxs-lookup"><span data-stu-id="33f58-115">This uses MAPI's ability to keep idle form instances running in an invisible state until a form of that form server's message class is activated.</span></span> <span data-ttu-id="33f58-116">En otras palabras, se pueden almacenar en caché los servidores de formulario en la memoria RAM para minimizar el número de veces que debe ser que se encuentra dentro de una biblioteca de formularios ejecutable de un formulario y se ha cargado en la memoria desde el disco o a través de la red.</span><span class="sxs-lookup"><span data-stu-id="33f58-116">In other words, form servers can be cached in RAM to minimize the number of times a form's executable must be located within a form library and loaded into memory from disk or over the network.</span></span> <span data-ttu-id="33f58-117">Al igual que la memoria caché la instancia de disco, la memoria caché de instancia que se está ejecutando se comporta de forma menos frecuente para que una instancia de formulario que se está ejecutando se puede purgar de la memoria caché para dejar espacio para otra instancia de formulario.</span><span class="sxs-lookup"><span data-stu-id="33f58-117">Like the disk instance cache, the running instance cache behaves in a least-frequently-used fashion so that a running form instance can be purged from the cache to make room for another form instance.</span></span> <span data-ttu-id="33f58-118">Esta caché se busca una instancia en ejecución de un servidor de formulario antes de que las bibliotecas de formularios se buscan en el servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="33f58-118">This cache is searched for a running instance of a form server before the form libraries are searched for the form server.</span></span>
  
> [!NOTE]
> <span data-ttu-id="33f58-119">El Administrador de formulario predeterminado muestra un indicador de progreso al instalar un formulario en la estación de trabajo de un usuario, lo que permite al usuario cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="33f58-119">The default form manager displays a progress indicator when installing a form on a user's workstation, enabling the user to cancel the operation.</span></span> <span data-ttu-id="33f58-120">Esto es especialmente útil si la conexión del usuario al archivo ejecutable del servidor de formulario es a través de una red de ancho de banda bajo.</span><span class="sxs-lookup"><span data-stu-id="33f58-120">This is especially useful if the user's connection to the form server's executable file is over a low bandwidth network.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="33f58-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="33f58-121">See also</span></span>

- [<span data-ttu-id="33f58-122">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="33f58-122">MAPI Forms</span></span>](mapi-forms.md)
