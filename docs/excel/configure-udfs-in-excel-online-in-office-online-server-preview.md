---
title: Configurar las UDF en Excel en línea en Office Online Server
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Utilizar funciones definidas por el usuario (UDF) de Excel en línea en Office Online Server para llamar a funciones personalizadas.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722791"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="fbe03-103">Configurar las UDF en Excel en línea en Office Online Server</span><span class="sxs-lookup"><span data-stu-id="fbe03-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="fbe03-104">Utilizar funciones definidas por el usuario (UDF) de Excel en línea en Office Online Server para llamar a funciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fbe03-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="fbe03-105">Funciones definidas por el usuario (UDF) de Excel Online permiten llamar a funciones personalizadas escritas en código administrado mediante el uso de las fórmulas en las celdas.</span><span class="sxs-lookup"><span data-stu-id="fbe03-105">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells.</span></span> <span data-ttu-id="fbe03-106">Puede usar las UDF para:</span><span class="sxs-lookup"><span data-stu-id="fbe03-106">You can use UDFs to:</span></span>
  
- <span data-ttu-id="fbe03-107">Llamar a funciones matemáticas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fbe03-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="fbe03-108">Obtener datos de orígenes de datos personalizados en hojas de cálculo.</span><span class="sxs-lookup"><span data-stu-id="fbe03-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="fbe03-109">Llamar a servicios web.</span><span class="sxs-lookup"><span data-stu-id="fbe03-109">Call web services.</span></span>
    
<span data-ttu-id="fbe03-110">Puede instalar los archivos binarios UDF en una de estas dos ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="fbe03-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="fbe03-111">Un directorio local.</span><span class="sxs-lookup"><span data-stu-id="fbe03-111">A local directory.</span></span> <span data-ttu-id="fbe03-112">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="fbe03-112">For example:</span></span> 
    
    <span data-ttu-id="fbe03-113">C:\UDFs\MySampleUdf.dll </span><span class="sxs-lookup"><span data-stu-id="fbe03-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="fbe03-114">La caché de ensamblados global.</span><span class="sxs-lookup"><span data-stu-id="fbe03-114">The global assembly cache.</span></span> <span data-ttu-id="fbe03-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="fbe03-115">For example:</span></span> 
    
    <span data-ttu-id="fbe03-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="fbe03-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="fbe03-117">Hacer referencia a la ubicación cuando se crea una definición de **New-OfficeWebAppsExcelUserDefinedFunction** en el servidor de Office Online.</span><span class="sxs-lookup"><span data-stu-id="fbe03-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fbe03-118">Office Online Server no es compatible con UDF que se encuentra en recursos compartidos de red.</span><span class="sxs-lookup"><span data-stu-id="fbe03-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="fbe03-119">Habilitar las UDF en servidor de Office Online</span><span class="sxs-lookup"><span data-stu-id="fbe03-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="fbe03-120">Cuando un administrador crea una nueva granja de servidores de Office Web Apps Server mediante el cmdlet [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, los ensamblados de UDF están deshabilitados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fbe03-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="fbe03-121">El valor predeterminado de la marca de **ExcelUdfsAllowed** es false.</span><span class="sxs-lookup"><span data-stu-id="fbe03-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="fbe03-122">Para habilitar las UDF, ejecute el siguiente comando de Windows PowerShell en el servidor de Office Online, después de haber creado la granja de servidores de Office Web Apps Server.</span><span class="sxs-lookup"><span data-stu-id="fbe03-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="fbe03-123">Crear definiciones de las UDF en servidor de Office Online</span><span class="sxs-lookup"><span data-stu-id="fbe03-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="fbe03-124">Después de habilitar las UDF, debe crear una definición para el archivo binario que contiene las UDF.</span><span class="sxs-lookup"><span data-stu-id="fbe03-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="fbe03-125">Para crear una definición para su UDF binario en el servidor en línea de Office, use el cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** .</span><span class="sxs-lookup"><span data-stu-id="fbe03-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="fbe03-126">Este cmdlet incluye los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="fbe03-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="fbe03-127">**Ensamblado**</span><span class="sxs-lookup"><span data-stu-id="fbe03-127">**Assembly**</span></span>
    
- <span data-ttu-id="fbe03-128">**UbicaciónDeEnsamblado**</span><span class="sxs-lookup"><span data-stu-id="fbe03-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="fbe03-129">**Habilitar** (se establece en False de forma predeterminada)</span><span class="sxs-lookup"><span data-stu-id="fbe03-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="fbe03-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbe03-130">**Description**</span></span>
    
<span data-ttu-id="fbe03-131">Los siguientes ejemplos muestran cómo crear las definiciones de UDF.</span><span class="sxs-lookup"><span data-stu-id="fbe03-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="fbe03-132">Después de crear la nueva referencia UDF, ejecute **iisreset** en el servidor para seleccionar la referencia inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="fbe03-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="fbe03-133">Comandos de Windows PowerShell en Office Online Server UDF adicionales</span><span class="sxs-lookup"><span data-stu-id="fbe03-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="fbe03-134">Use los siguientes cmdlets de Windows PowerShell para trabajar con las UDF:</span><span class="sxs-lookup"><span data-stu-id="fbe03-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="fbe03-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (sin parámetros obligatorios) - devuelve una lista de definiciones de UDF que están configurados en el servidor de Office Online.</span><span class="sxs-lookup"><span data-stu-id="fbe03-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="fbe03-136">**Set-OfficeWebAppsExcelUserDefinedFunction** (El parámetro identity requiere) - establece las propiedades en las definiciones de UDF existentes.</span><span class="sxs-lookup"><span data-stu-id="fbe03-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="fbe03-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (El parámetro identity requiere) - quita las definiciones de UDF existentes.</span><span class="sxs-lookup"><span data-stu-id="fbe03-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="fbe03-138">Ejemplo UDF</span><span class="sxs-lookup"><span data-stu-id="fbe03-138">UDF sample</span></span>

<span data-ttu-id="fbe03-139">Los siguientes archivos proporcionan un libro de ejemplo que usa una UDF y el archivo UDF binario:</span><span class="sxs-lookup"><span data-stu-id="fbe03-139">The following files provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="fbe03-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): un libro de ejemplo que usa una UDF</span><span class="sxs-lookup"><span data-stu-id="fbe03-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
- <span data-ttu-id="fbe03-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): el archivo binario UDF</span><span class="sxs-lookup"><span data-stu-id="fbe03-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): the UDF binary</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fbe03-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fbe03-142">See also</span></span>

- [<span data-ttu-id="fbe03-143">Configurar las opciones administrativas Excel Online</span><span class="sxs-lookup"><span data-stu-id="fbe03-143">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="fbe03-144">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="fbe03-144">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

