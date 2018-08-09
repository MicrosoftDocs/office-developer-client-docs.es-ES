---
title: Desarrollar servidores de formulario MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 83d652f313e139b1c6bb628d1119edda03a70e23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816674"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="40765-103">Desarrollar servidores de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="40765-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="40765-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40765-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40765-105">En esta sección se describe el proceso de creación de servidor de formulario ejecutable y los archivos de configuración de formulario para la creación de formularios personalizados de MAPI.</span><span class="sxs-lookup"><span data-stu-id="40765-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="40765-106">Antes de leer esta sección, debe familiarizarse con la información de [Formularios de MAPI](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="40765-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="40765-107">Desarrollo de un servidor de formulario incluye los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="40765-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="40765-108">Decidir qué información va a contener el formulario y elegir un conjunto de propiedades para contener esa información.</span><span class="sxs-lookup"><span data-stu-id="40765-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="40765-109">Para obtener más información, vea [elegir establecer propiedad de un formulario](choosing-a-form-s-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="40765-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="40765-110">Diseño de una interfaz de usuario con la que los usuarios pueden interactuar con las propiedades del formulario.</span><span class="sxs-lookup"><span data-stu-id="40765-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="40765-111">Elección de una clase de mensaje y generar un identificador único de clase (CLSID).</span><span class="sxs-lookup"><span data-stu-id="40765-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="40765-112">Para obtener información general de las clases de mensajes, vea [Las clases de mensajes de MAPI](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="40765-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="40765-113">Para obtener más información acerca de las clases de mensajes y formularios, vea [Elegir una clase de mensaje](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="40765-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="40765-114">Implementación de las interfaces de formulario MAPI necesarias, así como cualquier interfaces opcionales que necesita su servidor de formulario en particular.</span><span class="sxs-lookup"><span data-stu-id="40765-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="40765-115">Para obtener más información, vea [Escribir código de servidor de formulario](writing-form-server-code.md).</span><span class="sxs-lookup"><span data-stu-id="40765-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="40765-116">Escritura de código de la interfaz de usuario para controlar la interacción del usuario con el objeto de formulario y las propiedades utiliza el formulario.</span><span class="sxs-lookup"><span data-stu-id="40765-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="40765-117">Creación de un archivo de configuración de formulario para el formulario.</span><span class="sxs-lookup"><span data-stu-id="40765-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="40765-118">Para obtener más información, vea el [Archivo de formato de formulario de los archivos de configuración](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="40765-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="40765-119">Instalando el formulario en los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="40765-119">Installing the form on users' computers.</span></span> <span data-ttu-id="40765-120">Para obtener más información, vea [instalar un formulario en una biblioteca](installing-a-form-into-a-library.md).</span><span class="sxs-lookup"><span data-stu-id="40765-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="40765-121">Es muy probable que llevará a cabo los pasos del 1 al 5 simultáneamente en lugar de realizarlas en secuencia.</span><span class="sxs-lookup"><span data-stu-id="40765-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="40765-122">El proceso de desarrollo de un servidor de formulario, al igual que muchos proyectos de programación, no es uno de que exista una secuencia especialmente bien definida.</span><span class="sxs-lookup"><span data-stu-id="40765-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="40765-123">Por ejemplo, la creación de un archivo de configuración de formulario se muestra como el segundo a último paso anterior, pero probablemente va a crear el archivo de configuración del formulario de forma incremental y se convertirán en más completa como agregar características a su servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="40765-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40765-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="40765-124">See also</span></span>



[<span data-ttu-id="40765-125">Conceptos MAPI</span><span class="sxs-lookup"><span data-stu-id="40765-125">MAPI Concepts</span></span>](mapi-concepts.md)

