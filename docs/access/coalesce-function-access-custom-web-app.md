---
title: Función COALESCE (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Devuelve la primera expresión que no es NULL de una lista de argumentos.
ms.openlocfilehash: af309d2330f5c3b3999a4d99d8f2ab2d6d7d61db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282274"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="a3c1c-103">Función COALESCE (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="a3c1c-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="a3c1c-104">Devuelve la primera expresión que no es NULL de una lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="a3c1c-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a3c1c-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="a3c1c-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a3c1c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3c1c-107">Syntax</span></span>

<span data-ttu-id="a3c1c-108">**Fusión** (*Valor*, [*valor*],..., [*valor*])</span><span class="sxs-lookup"><span data-stu-id="a3c1c-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="a3c1c-109">La función **Coalesce** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a3c1c-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="a3c1c-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="a3c1c-110">**Argument name**</span></span>|<span data-ttu-id="a3c1c-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3c1c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a3c1c-112">*Valor*</span><span class="sxs-lookup"><span data-stu-id="a3c1c-112">*Value*</span></span>  <br/> |<span data-ttu-id="a3c1c-113">Una expresión.</span><span class="sxs-lookup"><span data-stu-id="a3c1c-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3c1c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3c1c-114">Remarks</span></span>

<span data-ttu-id="a3c1c-115">Si todos los argumentos son NULL, **Coalesce** devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="a3c1c-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a3c1c-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3c1c-116">Example</span></span>

<span data-ttu-id="a3c1c-117">La siguiente expresión se usa como regla de validación de una tabla.</span><span class="sxs-lookup"><span data-stu-id="a3c1c-117">The following expression is used as the validation rule for a table.</span></span> <span data-ttu-id="a3c1c-118">La expresión garantiza que las entradas se realicen en los campos nombre, apellidos, correo electrónico, teléfono móvil, teléfono del trabajo, teléfono particular y compañía antes de confirmar un registro.</span><span class="sxs-lookup"><span data-stu-id="a3c1c-118">The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed.</span></span> <span data-ttu-id="a3c1c-119">Si alguno de los campos enumerados se deja en blanco, la función **Coalesce** devuelve null, lo que infringe la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="a3c1c-119">If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


