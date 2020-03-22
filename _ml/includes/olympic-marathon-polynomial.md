\ifndef{olympicMarathonPolynomial}
\define{olympicMarathonPolynomial}

\include{_ml/includes/olympic-marathon-data.md}

\editme

\subsection{Polynomial Fits to Olympic Data}

\setupcode{import numpy as np
from matplotlib import pyplot as plt
import mlai
import pods}

\code{basis = mlai.polynomial

data = pods.datasets.olympic_marathon_men()

x = data['X']
y = data['Y']

xlim = [1892, 2020]

basis=mlai.Basis(mlai.polynomial, number=1, data_limits=xlim)}

\setupplotcode{import teaching_plots as plot}
\plotcode{plot.rmse_fit(x, y, param_name='number', param_range=(1, 27), 
              model=mlai.LM, 
			  basis=basis,
              xlim=xlim, objective_ylim=[0, 0.8],
              diagrams='../slides/diagrams/ml')}

\setupdisplaycode{from ipywidgets import IntSlider}
\displaycode{pods.notebook.display_plots('olympic_LM_polynomial_number{num_basis:0>3}.svg',
                            directory='../slides/diagrams/ml', 
                            num_basis=IntSlider(1,1,27,1))}


\setupcode{import numpy as np
from matplotlib import pyplot as plt
import teaching_plots as plot
import mlai
import pods}

\code{basis = mlai.polynomial

data = pods.datasets.olympic_marathon_men()

x = data['X']
y = data['Y']

xlim = [1892, 2020]
max_basis = 27

ll = np.array([np.nan]*(max_basis))
sum_squares = np.array([np.nan]*(max_basis))
basis=mlai.Basis(mlai.polynomial, number=1, data_limits=xlim)}

\code{plot.rmse_fit(x, y, param_name='number', param_range=(1, 28), 
              model=mlai.LM, basis=basis, 
              xlim=xlim, objective_ylim=[0, 0.8],
              diagrams='../slides/diagrams/ml')}

\displaysetupcode{import pods
from ipywidgets import IntSlider}
\displaycode{pods.notebook.display_plots('olympic_LM_polynomial_number{num_basis:0>3}.svg',
                            directory='../slides/diagrams/ml', 
                            num_basis=IntSlider(1,1,28,1))}
                            



\slides{
\define{width}{80%}
\define{animationName}{olympic_LM_polynomial_number}
\startanimation{\animationName}{1}{26}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number001}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number002}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number003}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number004}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number005}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number006}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number007}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number008}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number009}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number010}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number011}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number012}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number013}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number014}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number015}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number016}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number017}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number018}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number019}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number020}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number021}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number022}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number023}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number024}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number025}{\width}}{\animationName}
\newframe{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number026}{\width}}{\animationName}
\endanimation
}

\notes{\figure{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number002}{80%}}{Fit of a 1 degree polynomial to the olympic marathon data.}{olympic-lm-polynomial-num-basis-02}}

\notes{\figure{\includediagram{../slides/diagrams/ml/olympic_LM_polynomial_number003}{80%}}{Fit of a 2 degree polynomial to the olympic marathon data.}{olympic-lm-polynomial-num-basis-03}}



                            
\endif