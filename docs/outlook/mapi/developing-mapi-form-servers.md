---
title: Desarrollo de servidores de formulario MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420769"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="758e3-103">Desarrollo de servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="758e3-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="758e3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="758e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="758e3-105">En esta sección se describe el proceso de creación de archivos ejecutables y de configuración de formularios del servidor de formularios para crear formularios MAPI personalizados.</span><span class="sxs-lookup"><span data-stu-id="758e3-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="758e3-106">Antes de leer esta sección, debe familiarizarse con la información en [formularios MAPI.](mapi-forms.md)</span><span class="sxs-lookup"><span data-stu-id="758e3-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="758e3-107">El desarrollo de un servidor de formularios incluye los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="758e3-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="758e3-108">Decidir qué información contendrá el formulario y elegir un conjunto de propiedades para contener esa información.</span><span class="sxs-lookup"><span data-stu-id="758e3-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="758e3-109">Para obtener más información, vea [Eligiendo el conjunto de propiedades de un formulario.](choosing-a-form-s-property-set.md)</span><span class="sxs-lookup"><span data-stu-id="758e3-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="758e3-110">Diseño de una interfaz de usuario con la que los usuarios pueden interactuar con las propiedades del formulario.</span><span class="sxs-lookup"><span data-stu-id="758e3-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="758e3-111">Elegir una clase de mensaje y generar un identificador de clase único (CLSID).</span><span class="sxs-lookup"><span data-stu-id="758e3-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="758e3-112">Para obtener información general sobre las clases de mensajes, vea [Clases de mensajes MAPI.](mapi-message-classes.md)</span><span class="sxs-lookup"><span data-stu-id="758e3-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="758e3-113">Para obtener más información acerca de las clases de mensajes y los formularios, vea [Elegir una clase de mensaje](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="758e3-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="758e3-114">Implementar las interfaces de formulario MAPI necesarias, así como las interfaces opcionales que necesita el servidor de formularios en particular.</span><span class="sxs-lookup"><span data-stu-id="758e3-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="758e3-115">Para obtener más información, vea [Escritura de código de servidor de formulario.](writing-form-server-code.md)</span><span class="sxs-lookup"><span data-stu-id="758e3-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="758e3-116">Escribir código de interfaz de usuario para controlar la interacción del usuario con el objeto de formulario y las propiedades que usa el formulario.</span><span class="sxs-lookup"><span data-stu-id="758e3-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="758e3-117">Crear un archivo de configuración de formulario para el formulario.</span><span class="sxs-lookup"><span data-stu-id="758e3-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="758e3-118">Para obtener más información, vea [Formato de archivo de archivos de configuración de formulario.](file-format-of-form-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="758e3-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="758e3-119">Instalar el formulario en los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="758e3-119">Installing the form on users' computers.</span></span> <span data-ttu-id="758e3-120">Para obtener más información, vea [Instalar un formulario en una biblioteca.](installing-a-form-into-a-library.md)</span><span class="sxs-lookup"><span data-stu-id="758e3-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="758e3-121">Lo más probable es que realice los pasos del 1 al 5 simultáneamente en lugar de completarlos en secuencia.</span><span class="sxs-lookup"><span data-stu-id="758e3-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="758e3-122">El proceso de desarrollo de un servidor de formularios, como muchos proyectos de programación, no es uno en el que hay una secuencia especialmente bien definida.</span><span class="sxs-lookup"><span data-stu-id="758e3-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="758e3-123">Por ejemplo, la creación de un archivo de configuración de formulario se muestra como el último paso anterior, pero probablemente creará el archivo de configuración de formulario de forma incremental y se completará a medida que agregue características al servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="758e3-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="758e3-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="758e3-124">See also</span></span>



[<span data-ttu-id="758e3-125">Conceptos de MAPI</span><span class="sxs-lookup"><span data-stu-id="758e3-125">MAPI Concepts</span></span>](mapi-concepts.md)

